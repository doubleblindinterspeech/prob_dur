# Should you use a probabilistic duration model in TTS? Probably!\\{}Especially for spontaneous speech

> Converting input symbols to output audio in TTS requires modelling the durations of speech sounds. Leading non-autoregressive (NAR) TTS models treat duration modelling as a regression problem. The same utterance is then spoken with identical timings every time, unlike when a human speaks. Probabilistic models of duration have been proposed, but evidence of their benefits is, at best, mixed. However, prior studies generally only consider speech read aloud, and ignore spontaneous speech, despite the latter being both a more common and a more variable mode of speaking. We compare the effect of conventional deterministic duration modelling to durations sampled from a strong probabilistic model based on conditional flow matching (OT-CFM), in three different NAR TTS approaches: regression-based, deep generative, and end-to-end. Across four different corpora, stochastic duration modelling consistently improves probabilistic NAR TTS approaches, especially for spontaneous speech.



<style type="text/css">
    .tg {
    border-collapse: collapse;
    border-color: #9ABAD9;
    border-spacing: 0;
  }

  .tg td {
    background-color: #EBF5FF;
    border-color: #9ABAD9;
    border-style: solid;
    border-width: 1px;
    color: #444;
    font-family: Arial, sans-serif;
    font-size: 14px;
    overflow: hidden;
    padding: 0px 20px;
    word-break: normal;
    font-weight: bold;
    vertical-align: middle;
    horizontal-align: center;
    white-space: nowrap;
  }

  .tg th {
    background-color: #000000;
    border-color: #9ABAD9;
    border-style: solid;
    border-width: 1px;
    color: #fff;
    font-family: Arial, sans-serif;
    font-size: 14px;
    font-weight: normal;
    overflow: hidden;
    padding: 0px 20px;
    word-break: normal;
    font-weight: bold;
    vertical-align: middle;
    horizontal-align: center;
    white-space: nowrap;
    padding: 10px;
    margin: auto;
  }

  .tg .tg-0pky {
    border-color: inherit;
    text-align: center;
    vertical-align: top,
  }

  .tg .tg-fymr {
    border-color: inherit;
    font-weight: bold;
    text-align: center;
    vertical-align: top
  }
  .slider {
  -webkit-appearance: none;
  width: 75%;
  height: 15px;
  border-radius: 5px;
  background: #d3d3d3;
  outline: none;
  opacity: 0.7;
  -webkit-transition: .2s;
  transition: opacity .2s;
}

.slider::-webkit-slider-thumb {
  -webkit-appearance: none;
  appearance: none;
  width: 25px;
  height: 25px;
  border-radius: 50%;
  background: #409cff;
  cursor: pointer;
}

.slider::-moz-range-thumb {
  width: 25px;
  height: 25px;
  border-radius: 50%;
  background: #409cff;
  cursor: pointer;
}

audio {
    width: 240px;
}

/* CSS */
.button-12 {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 6px 14px;
  font-family: -apple-system, BlinkMacSystemFont, 'Roboto', sans-serif;
  border-radius: 6px;
  border: none;

  background: #6E6D70;
  box-shadow: 0px 0.5px 1px rgba(0, 0, 0, 0.1), inset 0px 0.5px 0.5px rgba(255, 255, 255, 0.5), 0px 0px 0px 0.5px rgba(0, 0, 0, 0.12);
  color: #DFDEDF;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
}

.button-12:focus {
  box-shadow: inset 0px 0.8px 0px -0.25px rgba(255, 255, 255, 0.2), 0px 0.5px 1px rgba(0, 0, 0, 0.1), 0px 0px 0px 3.5px rgba(58, 108, 217, 0.5);
  outline: 0;
}

video {
  margin: 1em;
}


</style>

# Prompt to generate sentences

## Corpus
<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky" colspan="2">Read</th>
    <th class="tg-0pky" colspan="2">Spontaneous</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>
      <button class="button-12" role="button" onclick="update_corpus_prompt('LJ Speech')" >
        LJ Speech
      </button>
    </td>
    <td>
      <button class="button-12" role="button" onclick="update_corpus_prompt('Ryan Speech')" >
        Ryan Speech
      </button>
    </td>
    <td>
      <button class="button-12" role="button" onclick="update_corpus_prompt('Trinity Speech and Gesture Dataset II')" >
        Trinity Speech and Gesture Dataset II
      </button>
    </td>
    <td>
      <button class="button-12" role="button" onclick="update_corpus_prompt('AptSpeech')" >
        AptSpeech
      </button>
    </td>
  </tr>
</tbody>
</table>

<script>

let corpus_prompt = {
    'LJ Speech' : `Take these sentence for example:
                    \`\`\`
                    The prisoners were in due course transferred to Newgate, to be put upon their trial at the Central Criminal Court.
                    They had to handcuff her by force against the most violent resistance, and still she raged and stormed,
                    The Secret Service has attempted to perform this function through the activities of its Protective Research Section
                    But the affair still remained a profound mystery. No light was thrown upon it till, towards the end of March,
                    Yet the public opinion of the whole body seems to have checked dissipation.
                    the Presidential limousine arrived at the emergency entrance of the Parkland Hospital at about twelve:thirty-five p.m.
                    Oswald was arrested and jailed by the New Orleans Police Department for disturbing the peace, in connection with a street fight which broke out when he was accosted
                    gaming of all sorts should be peremptorily forbidden under heavy pains and penalties.
                    we have reached into the heart of the problem which is to provide such annual earnings for the lowest paid worker as will meet his minimum needs.
                    it had established periodic regular review of the status of four hundred individuals;
                    who was one of the first witnesses to alert the police to the Depository as the source of the shots, as has been discussed in chapter three.
                    were governed by rules which they themselves had framed, and under which subscriptions were levied
                    might have been more alert in the Dallas motorcade if they had retired promptly in Fort Worth.
                    .
                    .
                    .
                    100 sentences
                    \`\`\`

                    Generate 100 sentences in a similar writing style. Talk about going to the zoo, going to a shopping centre or a mall and a day at the school. Make sure it looks like the text is from a similar speaker. Same conversational style try to match the speaker characteristics as much as you can.
                    `,
    'Ryan Speech': `

                Take these sentence for example:
                \`\`\`
                No, my friends keep me company.
                It grows somewhat like the lily of the valley, but its height is about three feet.
                Do you want to add anything to the order?
                Do you mean you are from England or you speak English?
                Could I be doing something different to make this more enjoyable?
                And could I book those flights for the morning, if possible?
                Even the creatures of the wood knew and loved him, for he never hurt anything that God had made.
                With logs of trees, a few hurdles, and other field appliances, a rustic banqueting hall was prepared and everything was very nice.
                Yes, they are playing at seven ten p m against the Cubs.
                They did not touch me, but merely showed the natural curiosity which is felt at the sight of a foreigner who has appeared unexpectedly.
                From paradise, I think, said Otto, with that patient seriousness that he had caught from the monks, and that sat so quaintly upon him.
                Why does unscented hair spray smell?
                I was at school in Canton Berne; it is a mother tongue to me.

                .
                .
                .
                100 sentences
                \`\`\`

                Generate 100 sentences in a similar writing style. Talk about going to the zoo and going to a shopping centre or a mall. Make sure it looks like the text is from a similar speaker

                `,

    'Trinity Speech and Gesture Dataset II': `

              Take these sentence for example:
              \`\`\`
              ; , Finish at like six; , or maybe seven or eight; then we'd all go out, you know have a few drinks head out to a nightclub or something like that come home.
              ; a bit of a; kind of a short story rather than just one scene; So all the class we all got together, the base was because every time we went to a new class.
              ; , And then all of a sudden the cameras came on and Leonardo DiCaprio was like; Just sitting like this just blocking himself, ; , And we're like oh shit it's Leonardo DiCaprio And then he was literally just like, ;
              ; for six months, in relation to college, I went over to a place called; , Old Westbury Golf and Country Club in Long Island So I stayed there for six months.
              I don't know if he looks at it as a regret, ; But the way he was talking about it you could see he was saddened by it; which kind of was, kind of puts things into perspective for you that like.
              We started off in Amsterdam; , So I went to Amsterdam Germany Poland; , Um; , Croatia Slovenia.
              people in the music industry, and; But I think I told you the story before but I'm going to tell it again anyway; Oh sorry even a better story than that.

              .
              .
              .
              total 100 sentences
              \`\`\`
              Generate 100 sentences in a similar conversational spontaneous style containing disfluencies, hesitations, repeats etc. With approximately similar lengths. Talk about going to the zoo, going to a shopping centre or a mall and talk about your day at the school.  Here ; is a breath and , is a pause use these too and generate syntactically similar sentences. Make it sound natural as one will do in conersational settings. Use fewer commas and fewer uh and uhm.


    `,
    'AptSpeech': `

              Take these sentence for example:
              \`\`\`
              And you can assume that all of the openings are doorways that will have doors that can open and close- So,
              Yes, and any room can be anything you want it to be. It's really up to you guys to decide how to divide up the space. so that you're comfortable living there.
              so we'd like to talk a little bit about maybe some good or maybe some bad experiences you've had with roommates.
              uh And I will be able to give you advice, because I am a world renowned interior decorator and designer,
              shopping centers starting with bedroom, kitchen, living room bathroom, rugs and miscellaneous.
              uh sharing a space with somebody. ; : Have you had a roommate in your life? : More than one time? : And what about you? Have you had more than,
              ; and that subject is, ; roommates, ; or flatmates, or anyone you've ever shared, ; a living space with, ;
              ; is we're going to have a conversation just between the three of us, ; and we're going to talk about a particular subject, ; and that subject is, ; roommates, ;
              And any issues uh sharing the like the combined space? Like say the living room, maybe you had a TV or a music system.
              My recommendation would be to start with the bedrooms again because these are bare essentials. Everyone must sleep - at least a few hours a night.
              or exercise or games or - things of that nature so there's plenty of stuff to, use the rooms for.
              ; and the reason we find this interesting is because it's a it's a tricky situation. : ; to sharing a space with someone but there can also be, ;
              there's lots of options when you go and look in the- furniture store, you'll see that there's a lot of items in the miscellaneous category,
              .
              .
              .
              100 sentences
              \`\`\`

              Generate 100 sentences in a similar writing style. Talk about going to the zoo and going to a shopping centre or a mall. Make sure it looks like the text is from a similar speaker. Same conversational style try to match the speaker characteristics as much as you can. Here ; is breath try to use it wisely. do not over use breathing (;) use it only where it would be appropriate.  Create sentences to train a TTS model so it should not be too long and not too short too something that can be 10-11 seconds.
    `

}

function update_corpus_prompt(corpus_name){
    let p_id = document.getElementById('corpus-prompt');
    let span_id = document.getElementById('corpus-prompt-name-span');

    p_id.innerHTML = corpus_prompt[corpus_name];
    span_id.innerHTML = corpus_prompt;
}

</script>

### Prompt: <span id="corpus-prompt-name-span"> LJ </span>

<blockquote>
    <p id="corpus-prompt">

        Take these sentence for example:

        ```
        The prisoners were in due course transferred to Newgate, to be put upon their trial at the Central Criminal Court.
        They had to handcuff her by force against the most violent resistance, and still she raged and stormed,
        The Secret Service has attempted to perform this function through the activities of its Protective Research Section
        But the affair still remained a profound mystery. No light was thrown upon it till, towards the end of March,
        Yet the public opinion of the whole body seems to have checked dissipation.
        the Presidential limousine arrived at the emergency entrance of the Parkland Hospital at about twelve:thirty-five p.m.
        Oswald was arrested and jailed by the New Orleans Police Department for disturbing the peace, in connection with a street fight which broke out when he was accosted
        gaming of all sorts should be peremptorily forbidden under heavy pains and penalties.
        we have reached into the heart of the problem which is to provide such annual earnings for the lowest paid worker as will meet his minimum needs.
        it had established periodic regular review of the status of four hundred individuals;
        who was one of the first witnesses to alert the police to the Depository as the source of the shots, as has been discussed in chapter three.
        were governed by rules which they themselves had framed, and under which subscriptions were levied
        might have been more alert in the Dallas motorcade if they had retired promptly in Fort Worth.
        .
        .
        .
        100 sentences
        ```

        Generate 100 sentences in a similar writing style. Talk about going to the zoo, going to a shopping centre or a mall and a day at the school. Make sure it looks like the text is from a similar speaker. Same conversational style try to match the speaker characteristics as much as you can.


</p>
</blockquote>

