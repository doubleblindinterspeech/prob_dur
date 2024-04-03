# Should you use a probabilistic duration model in TTS? Probably! Especially for spontaneous speech

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

# Generated sentences and their prompts



## Read-aloud speech

### LJ Speech

<details>

<summary>Prompt</summary>

```
Take these sentence for example:

~~~
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
<100 sentences>
~~~

Generate 100 sentences in a similar writing style. Talk about going to the zoo, going to a shopping centre or a mall and a day at the school. Make sure it looks like the text is from a similar speaker. Same conversational style try to match the speaker characteristics as much as you can.
```

</details>

<details>
<summary>Generated sentences</summary>

```
The family, in anticipation of a delightful day, set forth to the zoological gardens, a repository of nature's marvels.
Upon entering the grand gates of the shopping centre, they were greeted by a cacophony of sounds, each store vying for attention.
The majestic lion, king of the animal kingdom, lay in repose under the shade of an ancient oak, barely acknowledging the gathered spectators.
This journey from classroom to zoo to mall taught one vital lesson: learning thrives not just in silence and books but in the lively embrace of the world's vast wonders.
Children, with eyes wide with wonder, pressed their faces against the glass of the aquarium, mesmerized by the dance of the tropical fish.
In the food court, a veritable feast was laid out, offering delicacies from the far corners of the earth, each stall a testament to the culinary diversity of mankind.
The elephant, with its ponderous gait and wise eyes, seemed to carry the wisdom of the ages as it slowly made its way to the watering hole.
The milliner's shop, with its array of bonnets and hats, seemed a throwback to a time when headwear was a symbol of one's status in society.
The shrill cries of the monkeys in their enclosure provided a stark contrast to the otherwise serene ambiance of the zoo.
Bargain hunters thronged the aisles of the clearance sale, each in search of that elusive deal that would mark the day's triumph.
The giraffes, with their long necks stretching towards the heavens, seemed to be in a world of their own, aloof from the gaze of the onlookers.
The scent of freshly baked bread from the bakery mingled with the perfume of the florist, creating an olfactory tapestry that enveloped the shoppers.
The reptile house, with its dimly lit corridors and the silent watchfulness of its inhabitants, evoked a sense of mystery and ancient lore.
The jeweler, with a craftsman's eye, meticulously arranged the display, each piece a testament to human artistry and the allure of precious stones.
The peacocks, with their plumage in full display, strutted with an air of vanity, seemingly aware of their unrivaled beauty.
The bookshop, a haven of tranquility amidst the hustle and bustle, offered the promise of worlds waiting to be discovered within the pages of its tomes.
The ice cream vendor, with his cart adorned with pictures of frozen delights, became the center of attention as children clamored for a sweet treat.
The fragrance section of the department store enveloped shoppers in a cloud of scents, each vial containing the essence of dreams and memories.
The penguins, with their comedic waddle, provided a moment of levity, their antics a reminder of nature's capacity for joy.
The antique shop, a treasure trove of history's artifacts, invited the curious to delve into the stories of objects left behind by time.
The butterfly enclosure, a kaleidoscope of color, offered a moment of enchantment as these delicate creatures flitted from flower to flower.
In the toy shop, generations of toys stood in silent testimony to the changing tides of children's fantasies and the timeless joy of play.
The zoo's aviary, a symphony of birdcalls, was a reminder of the vastness of nature's palette, each species a unique note in the harmony of life.
The café, with its promise of refreshment, became a gathering place for weary shoppers, a brief respite in their quest for commerce.
As the day waned, the families, laden with purchases and memories, made their way home, their hearts full from the day's adventures in the realms of nature and commerce.
Upon entering the grand gates of the local zoo, one is immediately struck by the cacophony of sounds, a vivid testament to the diversity housed within.
The majestic lions, in their enclosures, lay with a regal indifference, surveying their kingdom with lazy, half-closed eyes.
Children, their faces alight with wonder, pressed eagerly against the glass of the reptile house, their breath fogging up the surface.
It was a marvel to observe the agile monkeys, who, with deft leaps and bounds, seemed to mock the gravity that bound the rest of us earthward.
The zookeepers, with a patience born of routine, answered the myriad questions posed by curious onlookers, their knowledge deep and detailed.
Amidst the aviary's dense foliage, the flash of vibrant plumage revealed the presence of exotic birds, their songs a melody of the wild.
As the afternoon waned, the crowd at the elephant exhibit grew, each visitor eager to witness the gentle giants' graceful movements.
The chill of the aquarium's halls contrasted sharply with the outdoor warmth, its blue lights casting an otherworldly glow on fascinated faces.
At the penguin enclosure, the birds' comedic waddle elicited laughter and delight, a welcome relief from the more somber moods of some exhibits.
The gift shop, strategically placed at the zoo's exit, offered an array of souvenirs, each item a tangible memory of the day's adventures.
The vast expanse of the shopping center loomed ahead, its many stores promising untold treasures to those willing to explore.
The hum of conversation filled the air, a constant backdrop to the clatter of shopping carts and the soft shuffle of feet on polished floors.
In the food court, the mingling aromas of a dozen different cuisines created a tantalizing invitation to dine.
Sales signs, bold and beckoning, adorned the windows of every shop, each one a siren call to bargain hunters.
The mall's central atrium, adorned with seasonal decorations, became a gathering place for weary shoppers seeking a moment's rest.
Teenagers roamed in packs, their laughter echoing off the high ceilings, a hallmark of the freedom found in such communal spaces.
Parents, their patience stretched thin, navigated the crowds with strollers in tow, their journeys marked by frequent stops and starts.
The latest fashion trends were on full display, mannequins dressed in the height of style, silently inviting onlookers to update their wardrobes.
Occasionally, a street performer would captivate an impromptu audience, their artistry adding a layer of unexpected delight to the shopping experience.
As night fell, the shopping center's lights shimmered like stars, transforming the complex into a beacon for those seeking late-night entertainment.
The morning's light barely crept through the classroom windows as students shuffled in, the day's lessons a looming presence in their minds.
In the corridors, the echo of footsteps mingled with the distant sound of a bell, heralding the start of another academic venture.
The chalk's screech against the blackboard filled the room, each word written by the teacher a testament to the day's learning objectives.
Students huddled over textbooks, their brows furrowed in concentration, a silent battle against the complexities of new knowledge.
The library stood as a sanctuary of silence, its shelves laden with the weight of words, a haven for those seeking solace in study.
Lunchtime brought a cacophony of sounds to the cafeteria, the clatter of trays and the murmur of conversations a welcome interlude.
On the playground, the air was filled with the shouts and laughter of children, a brief escape from the confines of the classroom.
Teachers patrolled the halls with a vigilant gaze, their presence a constant reminder of the order that governed the school's daily life.
In the science lab, the smell of chemicals mingled with the sense of anticipation, each experiment a journey into the unknown.
Art class revealed a burst of color against the school's otherwise monochrome backdrop, creativity blooming amidst strict schedules.
The gym echoed with the sound of sneakers on wood, the physical exertion a counterbalance to the day's mental challenges.
History lessons unfolded like stories, the past coming alive through the teacher's words, a bridge across time.
Mathematics, with its numbers and equations, offered a puzzle for the mind, logic and reasoning entwined in a dance of digits.
The school bell's ring, a clarion call, signaled the end of one period and the start of another, a cyclical reminder of time's passage.
In the computer lab, screens glowed with the promise of technological exploration, fingers dancing over keyboards in digital discovery.
Language classes wove a tapestry of sounds, the nuances of grammar and vocabulary a challenge to master.
The school counselor's office offered a haven of advice, a guiding light for those navigating the tumultuous waters of adolescence.
As the final bell rang, the rush of students towards the exit was a torrent of relief, the promise of home a sweet end to the day.
Homework assignments, like seeds of knowledge, were planted in the minds of students, destined to grow in the soil of their intellect.
School buses lined up like sentinels, their engines humming a song of departure, ready to ferry their charges back to the comforts of home.
Extracurricular activities flourished in the after-school hours, each club and team a microcosm of shared interests and talents.
The setting sun cast long shadows across the schoolyard, a quiet reminder of the day's end and the passage of another page in the academic year.
Teachers gathered in the staff room, their conversation a blend of reflection and anticipation, the day's events a mosaic of triumphs and challenges.
The silence that settled over the empty classrooms was a stark contrast to the day's earlier bustle, a momentary pause in the cycle of education.
Lost items found their way to the school's lost and found, each one a story of forgetfulness and the hope of reunion.
The principal's office, often perceived as a place of authority and discipline, also served as the heart of the school's administrative life.
Bulletin boards, adorned with notices and achievements, offered a snapshot of school life, a collage of opportunities and accolades.
Parent-teacher meetings, scheduled in the calendar, promised a confluence of perspectives, a partnership in the educational journey.
The school's garden, tended by student volunteers, bloomed with the seasons, a living lesson in nature's cycles.
As night descended, the school stood silent and empty, a vessel of dreams and aspirations, waiting to be filled again with the dawn of a new day.
Early in the morning, the school organized a field trip, a journey that promised both education and entertainment, to the local zoo.
Students gathered at the entrance, their chatter blending with the distant calls of animals, a prelude to the day's adventures.
On their way, the bus passed by the city's sprawling shopping center, its vastness a reminder of commerce's reach.
Upon arrival, the sight of the majestic elephants immediately captivated the students, a living lesson in biology and conservation.
The teachers, acting as guides, pointed out the importance of each habitat, their words weaving knowledge into the fabric of experience.
In the reptile house, the students faced their fears, learning that understanding can turn apprehension into respect.
The gift shop at the zoo offered educational souvenirs, each item a memento of learning outside the classroom walls.
Meanwhile, a group of students tasked with a project on economics ventured into the shopping center, their observations aimed at understanding consumer behavior.
They noted the variety of stores, each catering to different needs and wants, a practical lesson in supply and demand.
The food court provided a study in choices and preferences, a live demonstration of market segmentation and targeting.
Back at the zoo, a keeper's talk on endangered species sparked a discussion among students about responsibility and environmental stewardship.
The aquarium's serene beauty offered a moment of reflection, the silent fish a contrast to the bustling corridors of the school.
As the day drew to a close, the students gathered for a sketching session, capturing the animals' forms, a blend of art and observation.
Returning to school, they passed the shopping center once more, its lights a beacon in the early evening, a symbol of the community's pulse.
The bus ride back was a buzz of excited conversations, each student sharing their day's highlight, a chorus of shared experiences.
Upon their return, the schoolyard, usually a scene of hurried departures, was a place of animated recounting, the field trip a bonding experience.
Teachers reminded students to pen down their reflections, an assignment that would bridge their experiences with their curricular studies.
In the following days, presentations were made, the zoo and shopping center visits transformed into educational showcases.
Students debated the ethics of zoos and the impact of consumerism, their classroom a forum for critical thinking and exchange.
Art projects inspired by the trip adorned the hallways, turning the school into a gallery of student creativity and insight.
The economics project group presented their findings, the shopping center's dynamics distilled into graphs and analyses.
Reflections on the endangered species talk led to a school-wide initiative on sustainability, the field trip sparking action.
The zoo visit, once merely an outing, became a catalyst for a deeper understanding of biology, ecology, and environmental science.
The shopping center excursion, too, shed light on the practical applications of mathematics, social studies, and economics.
As the term progressed, the memories of the field trip lingered, a reminder of the day when the zoo and the mall became classrooms without walls.
```
</details>

### Ryan Speech


<details>

<summary>Prompt</summary>

```
Take these sentence for example:

~~~
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
~~~

Generate 100 sentences in a similar writing style. Talk about going to the zoo and going to a shopping centre or a mall. Make sure it looks like the text is from a similar speaker

```

</details>


<details>

<summary>Generated sentences</summary>

```
The lions at the zoo roared loudly, as if they were greeting us personally upon our arrival.
I couldn't help but marvel at the vibrant colors of the parrots, chatting away in their enclosure.
Do you think the elephants enjoy painting? I asked, watching one create a beautiful piece with its trunk.
The smell of fresh popcorn wafted through the air, leading us to the zoo's quaint little snack stand.
We found a bench by the monkey exhibit, perfect for a quick rest and some people-watching.
Should we buy a souvenir? I pondered aloud, eyeing the cute stuffed animals in the gift shop.
The aquarium section was mesmerizing, with its soothing blue lights and the graceful dance of the fish.
I had to chuckle at the zebras, who seemed to be engaged in their own version of a staring contest with us.
Look, the new tiger cubs! exclaimed my friend, as we hurried over to the big cat area.
It was feeding time for the giraffes, and we got to watch them stretch their long necks for lettuce.
I've always found the reptile house both eerie and fascinating, with its silent, watchful inhabitants.
The petting zoo was a hit with the children, their laughter mixing with the sounds of the animals.
I wonder what it's like to be a zookeeper, I mused, watching a worker tend to the flamingos.
The penguin parade was about to start, a daily highlight that drew a cheerful crowd.
We paused to admire the orchids in the zoo's tropical greenhouse, a riot of color and fragrance.
Shall we adopt an animal? the sign suggested, offering a way to support the zoo's conservation efforts.
As we left, the peacocks bid us farewell, their feathers a stunning display of nature's artistry.
The mall was bustling, a lively hub of shoppers and diners alike.
We made a beeline for the bookstore, a treasure trove of stories waiting to be discovered.
The food court offered a world tour of cuisines, making it hard to choose just one.
This sale is too good to miss! I overheard someone say, clutching a handful of discounted clothes.
The new tech store had the latest gadgets on display, drawing a crowd of eager customers.
I found a cozy corner in the coffee shop, perfect for people-watching and sipping my latte.
Do you want to try the virtual reality experience? my friend asked, pointing to a new setup near the center.
The aroma of freshly baked cookies led us to a small bakery, where we couldn't resist buying a dozen.
We stumbled upon a local artist's pop-up gallery, each piece more captivating than the last.
The ice skating rink was a whirl of motion, laughter echoing as skaters glided past.
Let's take a photo in the photo booth, suggested my friend, a fun way to capture our mall adventure.
The fashion show on the central stage was a dazzle of lights, music, and stunning outfits.
A group of street performers gathered a crowd, their acrobatic feats leaving everyone in awe.
I could spend hours in this place, I thought, admiring a shop dedicated entirely to exotic teas.
The mall's indoor garden was a peaceful retreat, complete with a trickling fountain and benches.
They have a workshop today on DIY jewelry, my friend noted, interested in the craft event.
We paused to watch a cooking demonstration, the chef's skills as impressive as the delicious samples.
Remember to validate your parking, a helpful sign reminded us, a small but important detail.
The children's play area was a hive of activity, a safe space for little ones to burn off energy.
Let's check the map, I suggested, realizing just how easy it was to get turned around in the sprawling mall.
A flash sale at the electronics store caused quite the stir, bargain hunters rushing in.
The luxury brand section was like stepping into another world, with its opulent displays and exclusive boutiques.
This place has the best smoothie bar, my friend claimed, leading the way to a hidden gem.
We signed up for the mall's loyalty program, enticed by the promise of discounts and special offers.
The seasonal decorations made the mall feel festive, from twinkling lights to oversized ornaments.
I've been looking for this book everywhere! I exclaimed, finally finding a rare edition in the second-hand.
The zoo was bustling with families, a true testament to its popularity among locals and tourists alike.
I couldn't help but admire the elegant flamingos, their pink feathers a stark contrast against the blue pond.
Isn't it fascinating how the monkeys swing with such ease, almost as if they're performing for an audience?
Our next stop has to be the lion's den; I've heard their roars can be heard across the entire zoo.
Do you think the gift shop will have those adorable plush elephants? My niece would love one.
Walking through the reptile house felt like stepping into another world, each enclosure a window to a different habitat.
I found myself captivated by the slow, graceful movements of the sea turtles in the aquarium section.
Would you like to grab a bite at the zoo cafe, or shall we pack our own picnic next time? I pondered aloud.
The map shows a bird aviary nearby, let's make sure to visit. I've always been intrigued by exotic birds.
Watching the penguins dive into the water is always a highlight for me; their antics are so playful and amusing.
Remember to wear comfortable shoes, I reminded my friend, knowing we'd be doing a lot of walking.
The idea of a guided tour sounds intriguing. Do you think we'll learn more about the animals that way?
I'm curious about the conservation efforts here. It's important to support zoos that prioritize animal welfare.
The souvenir shop was our last stop, a chance to bring home a piece of our memorable day.
As we left the zoo, I felt a renewed sense of wonder for the natural world and its inhabitants.
Transitioning to our mall adventure, the vibrant store displays immediately caught our eye.
Do you think the food court has that new sushi place? I asked, already craving something fresh and delicious.
The shopping center's layout was impressive, with wide aisles and plenty of seating areas for weary shoppers.
I couldn't resist stopping by the bookstore; there's something about browsing shelves that feels so comforting.
The mall's indoor garden was a peaceful retreat amid the hustle and bustle of shoppers.
Let's check out the electronics store for the latest gadgets, suggested my companion, eager for new tech.
Fashion boutiques lined the corridors, each window more enticing than the last.
We made a pact to only buy what we needed, but the seasonal sales were too good to pass up.
The aroma from the bakery was irresistible, leading us to indulge in freshly baked pastries.
How about a movie after shopping? The cinema's latest offerings promised a perfect end to our day.
The mall's art exhibit added a cultural touch to our visit, showcasing local talent.
Finding a parking spot was a challenge, a reminder of the mall's popularity on weekends.
I heard there's a new virtual reality arcade, my friend mentioned, excitement in their voice.
We laughed over ice cream cones, sharing stories and making plans for our next outing.
As we exited the mall, bags in hand, we couldn't help but feel content with our day's discoveries.
The jewelry store window glinted with promise, tempting us with its sparkling displays.
Shall we take a break and people-watch for a bit? It's always interesting to observe the mall's diverse crowd.
The children's play area was alive with laughter, a joyful sight that brought smiles to our faces.
We stumbled upon a pop-up shop selling handmade goods, a delightful find that supported local artisans.
The escalators offered a moment of rest, a brief pause as we moved between floors.
This place has everything, I mused, impressed by the variety of stores and services available.
The sound of live music led us to a small stage where a local band was performing, adding to the mall's lively atmosphere.
We made sure to visit the outdoor section of the mall, enjoying the blend of shopping and nature.
I could spend hours here, my friend said, echoing my thoughts about the mall's inviting environment.
As the day drew to a close, we reflected on our zoo and mall adventures, grateful for the memories made.
The morning bell echoed through the halls, signaling the start of another day filled with learning and discovery.
I hurried to my first class, clutching my notebook and pencil, eager to jot down the day's lessons.
The chemistry lab was a buzz of activity, with students mixing solutions and marveling at the reactions.
Do you understand this math problem? I whispered to my classmate, struggling with a particularly tricky equation.
Our history teacher brought the past to life, weaving tales of ancient civilizations with such passion and detail.
Lunchtime was a welcome break, a chance to recharge and share stories with friends under the warm sun.
The library's quiet corners offered a perfect escape for those moments when the world outside felt too loud.
I lost track of time browsing the shelves, each book a doorway to a different time and place.
Are you joining the after-school club meeting today? I was asked, reminded of the communities that thrived beyond the classroom.
The art room smelled of paint and possibility, a space where creativity knew no bounds.
Our teacher encouraged us to express ourselves freely, reminding us that there's no wrong way to create art.
The gym echoed with the sounds of bouncing balls and sneakers squeaking against the polished floor.
I cheered on my classmates during the basketball game, feeling a sense of pride and camaraderie.
As the afternoon sun cast long shadows, I noticed the beauty of the campus, with its sprawling grounds and ancient trees.
Homework club is a lifesaver, I thought, grateful for the extra help and the quiet space to study.
The science fair posters lined the hallway, each project a testament to the curiosity and hard work of my peers.
What's your project about? I asked, intrigued by the innovative ideas on display.
```

</details>


## Spontaneous speech

### Trinity Speech and Gesture Dataset II

<details>

<summary>Prompt</summary>

```
Take these sentence for example:

~~~
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
~~~

Generate 100 sentences in a similar conversational spontaneous style containing disfluencies, hesitations, repeats etc. With approximately similar lengths. Talk about going to the zoo, going to a shopping centre or a mall and talk about your day at the school.  Here ; is a breath and , is a pause use these too and generate syntactically similar sentences. Make it sound natural as one will do in conersational settings. Use fewer commas and fewer uh and uhm.

```

</details>

<details>
  <summary>Generated sentences</summary>

```
; I'm like, should we take photos? But my phone, it's dead, completely dead.
; And then, the elephants, they're huge, you know? Just massive.
; We're walking, and suddenly, this peacock just shows up, fanning its feathers.
; I'm trying to get a closer look, but, you know, there's this fence.
; Oh, and the gift shop, it was, kind of pricey, but I bought a keychain.
; We were starving, so we thought, let's grab a bite, but the line, it was so long.
; Then, we're leaving, and it starts to rain, just our luck, right?
; I saw this cute hat, but when I tried it on, it looked weird on me.
; We saw these kids, running around, screaming ; parents nowhere.
; And then, there's the ice cream stand, but I dropped mine, just plop on the ground.
; We thought about going to the aquarium section, but it was, like, closed for maintenance.
; So, we're at the mall now, and it's packed, I mean, really crowded.
; I'm looking for a parking spot, and it's like, there's none, just circles around.
; We finally find this one store, and they're having a sale but nothing in my size.
; My friend wants to check out this new electronics store, and I'm like, sure, why not?
; Then, this guy, he spills his drink, and it's everywhere, on the floor.
; We're about to leave, and my friend realizes, she lost her phone.
; So, we backtrack, everywhere we went, and finally, it's at the lost and found.
; And there's this kiosk, selling these quirky sunglasses, so I get a pair.
; We pass by this jewelry store, and there's this beautiful necklace, but, you know, too expensive.
; I'm trying on shoes, and this one pair, it's perfect, but the left one's tight.
; We're heading out, and there's this group of teenagers, just loud and everywhere.
; I remember, I wanted to buy this book, but the bookstore, it's gone, replaced.
; We see this advertisement for a movie, and we're like, should we watch it? But we're too tired.
; Oh, and the escalators, one of them was broken, so we had to take the stairs.
; I'm looking for a restroom, and when I find it, there's a line, of course.
; We wanted to sit and relax, but all the benches, they're taken, every single one.
; There's this new makeup store, and I'm like, let's just look, ended up buying lipstick.
; We're trying to find this specific shop, and we ask for directions, but it's confusing.
; And then, there's this sale sign, but when we get there, it ended yesterday.
; I wanted to buy a gift, but I'm indecisive, so I left with nothing.
; We're leaving the mall, and I realize, I forgot where we parked.
; Finally, we find the car, and it's like, we've been walking forever.
; So, back to the zoo, remember? There was this funny parrot, mimicking people.
; And I'm trying to get a video, but then it just stops, typical.
; We're at the reptile house, and it's cool, but kind of creepy, snakes everywhere.
; I wanted to see the pandas, but they're asleep, just our luck, again.
; We're at this exhibit, and there's supposed to be this rare bird, but we can't find it.
; Oh, and the map, it's confusing, we got lost, like, three times.
; There's this play area for kids, and it's chaotic, but the kids are having fun.
; We're about to watch this feeding show, but it's so crowded, can't see a thing.
; And then, we're leaving, and this bird, it poops, nearly misses me.
; So, we're hungry, and we find this place, but it's just hot dogs.
; And the zoo, it's closing, but we missed the last show, didn't know the time.
; We're exiting, and there's this huge line for the tram, so we walk.
; Back at the mall, we see this art exhibit, but it's closing in 10 minutes.
; There's this store, all about sports, and my friend's excited, but I'm bored.
; We try this new coffee place, and it's good, but took forever to get our order.
; And there's this contest, win something, but we never win those, didn't bother.
; We're looking for a bathroom again, and it's cleaner than I expected, thankfully.
; We pass by this pet store, and there are puppies, but we just look, can't have pets.
; And then, this store, it's playing loud music, but it's actually pretty good.
; We're about to go home, and I realize, I didn't buy what I came for.
; So, we're planning to go back, but maybe on a weekday, less people, hopefully.
; And that's it, our trip to the zoo and the mall, just a regular day, but fun.
; So, like, I get to school, right? And first thing, I forgot my math homework, just left it on the table.
; And there's this quiz in history, I'm like, barely awake, trying to remember dates and stuff.
; Lunchtime comes, and I'm sitting with my friends, and we're talking about this new game, everyone's obsessed.
; Then, in gym class, we're playing dodgeball, and I'm hit, like, immediately, out in the first round.
; I'm walking to the next class, and I see this poster for the school play, thinking maybe I should try out.
; So, English class, we're reading this book, and I actually like it, but I'm behind a few chapters.
; And there's this group project, right? But no one wants to take the lead, so it's kind of awkward.
; I'm at my locker, and it won't open, just stuck, and I'm pulling and pulling, finally, it pops open.
; Then, there's this assembly, supposed to be motivational, but it's just, you know, kind of boring.
; We're leaving the assembly, and everyone's trying to be the first out, just a huge crowd at the doors.
; And I'm thinking about the math homework I forgot, wondering if I can make up some excuse.
; So, after school, there's practice for the soccer team, and I'm late, sprinting across the field to join.
; And we're doing drills, and I'm trying, but I keep messing up, coach is not happy.
; Practice ends, and we're all tired, but we decide to go grab something to eat, just hang out.
; I'm on my way home, and I realize, I have this huge project due tomorrow, barely started.
; So, I'm home, right? And I'm trying to work on this project, but my computer decides to update.
; And I'm panicking, watching the update screen, just praying it finishes in time.
; Finally, it's done, and I'm typing as fast as I can, but it's like, I can't get my thoughts straight.
; I take a break, and I'm just staring out the window, thinking about how much I dislike group projects.
; Then, my friend calls, asking about the math homework, and I'm like, forgot it, can you help?
; We're on the phone, and she's trying to explain this math problem, but I'm just not getting it.
; So, it's getting late, and I'm still not done with the project, feeling stressed.
; And then, I remember, I have a science test too, just great, another thing to worry about.
; I'm trying to study for science, but all I can think about is how much I want to sleep.
; Then, I get a text from my friend, saying we should have studied together, missed opportunity.
; It's past midnight, and I'm finally done with the project, but now I need to study.
; I'm reading my science notes, and it's like, none of this is staying in my head.
; And I think, maybe a quick nap will help, but I'm worried I won't wake up in time.
; So, I set multiple alarms, just in case, and lay down, but my mind is racing.
; And I'm thinking about the day, all the things that went wrong, and what's waiting for me tomorrow.
; Eventually, I fall asleep, but it's not restful, keep waking up, checking the time.
; Morning comes, and I'm groggy, trying to remember everything I studied last night.
; I'm at breakfast, and I'm not really hungry, just nervous about the test and the project presentation.
; And I'm out the door, backpack heavy with books, hoping today will be better than yesterday.
; I get to school, and first thing, there's a pop quiz in English, didn't see that coming.
; And I'm sitting there, trying to remember what I read, but it's all a blur.
; Lunchtime, and I'm with my friends, but I can't stop thinking about the science test.
; Then, it's time for the test, and I'm looking at the questions, some of it's familiar, thankfully.
; After the test, I'm not sure how I did, just hoping for the best, really.
; And then, it's time for the project presentation, and our group is a mess, but we manage.
; School's finally over, and I'm walking out, feeling like I've survived a marathon.
; I'm on my way home, and I'm thinking, maybe I'll take it easy tonight, just relax.
; But then, I remember, I have homework in three subjects, no rest for the weary.
; So, I'm home, and I'm starting on homework, but first, a snack, need some energy.
; And I'm working, and it's not so bad, feeling a little better about things.
```
</details>

### AptSpeech

<details>

<summary>Prompt</summary>

```
Take these sentence for example:
~~~
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
~~~

Generate 100 sentences in a similar writing style. Talk about going to the zoo and going to a shopping centre or a mall. Make sure it looks like the text is from a similar speaker. Same conversational style try to match the speaker characteristics as much as you can. Here ; is breath try to use it wisely. do not over use breathing (;) use it only where it would be appropriate.  Create sentences to train a TTS model so it should not be too long and not too short too something that can be 10-11 seconds.

```

</details>

<details>

<summary>Generated sentences</summary>

```
So, visiting the zoo is like stepping into a whole new world, isn't it? Each exhibit is a doorway to a different habitat.
uh, And you know, you can decide to follow the map or just wander. It's really up to you to explore.
; So we'd like to talk about maybe some memorable or maybe some forgettable experiences you've had at the zoo.
And I can give you tips, because I've visited zoos all over the globe, from the savannas of Africa to the rainforests of Brazil.
Then there's the shopping center or mall, starting with the food court, clothing stores, electronics, home goods, and, uh, the miscellaneous shops.
Sharing a day out with someone at the zoo; have you ever done that? : Once? : More than once? : What about at the mall? Have you gone shopping with,
; and that's what's interesting, ; zoo visits and shopping trips, ; or any day out where you've shared the experience,
; we're going to have a chat, just between us, about those experiences, ; and specifically about, ; days out, ;
Any issues sharing the experience? Like navigating through crowds or deciding where to eat?
I'd recommend starting your zoo visit with the big attractions, like the lions or elephants. They're the main draws for a reason.
or maybe you're more into the shopping experience, looking for deals or the perfect outfit.
; and the reason this is fascinating is because it's a it's a mix of personal tastes and compromises when sharing these experiences,
There's a lot of options when you hit the mall - you'll see a wide variety in each store, especially in the 'new arrivals' sections,
you have to ask me- but as you can see, we have many options for spending the day - whether at the zoo or the mall,
have you ever had an experience, though, with someone who couldn't decide where to eat at the mall, and you just wandered aimlessly?
The food court can be a battleground, I'd say, because it's a spot everyone has an opinion on.
okay, well let's talk about those two destinations you just mentioned, the zoo and the mall.
mhm, sure - that actually leads us nicely into what we're planning next.
would you trade a zoo visit for a day at the mall? That's a tough choice for some.
The vibrant colors at the zoo are so natural - whereas the mall lights offer a more artificial ambiance.
well, considering your preferences might help. Let's see how that influences your choices, huh?
but remember, whatever you share on social media about your day out, we get to discuss here.
Yes, you can visit as many stores as you want, but remember, budget constraints mean you can't buy everything you like. : ;
no issues while exploring together, huh?
and let's start planning these outings, with some suggestions - so I'm just going to take you through some options. We've got two main destinations: the zoo and the mall.
I don't think there's a need to rush. Take your time to enjoy each moment.
And, uh, when you're at the zoo, don't you just love those moments when an animal comes right up to the glass? It's like they're greeting you personally.
So, how about when you find that perfect spot at the mall, right? The one store where everything just calls out to your style.
; Let's not forget, the parking situation - at the zoo or the mall - can make or break the start of your day.
I've got to say, the food options at the zoo have really stepped up; it's not just about snacks anymore but a whole dining experience.
uh, And if you're at the mall, do you prefer the big department stores or the unique, boutique shops?
; Planning your route through the zoo can be as strategic as planning your shopping spree to catch all the best sales.
The energy at the zoo early in the morning is unbeatable, with all the animals just waking up.
Or the calmness of the mall just as it opens, when the stores are all pristine and the crowds haven't arrived yet.
uh, Have you ever had that moment at the zoo when the weather just does a complete turnaround? Always brings a sense of adventure.
; And, talking about weather, the mall is a great escape on those days - endless entertainment without worrying about rain or shine.
You know, there's always that one exhibit at the zoo that you find yourself returning to, time and again.
Similarly, there's that one store in the mall that seems to have a magnetic pull, right?
; I always find it interesting to watch how people interact with the animals at the zoo, those moments of connection.
And at the mall, it's fascinating to observe the latest trends catching everyone's attention.
uh, The souvenir shops at the zoo are like treasure troves, each item telling a story of conservation and wonder.
Just like the specialty stores in the mall, where you can find those one-of-a-kind items that just scream 'you'.
; Ever noticed how a day at the zoo can make you forget all your worries? It's like a mini-vacation.
And how a successful shopping trip can give you that sense of accomplishment, like you've conquered the mall.
uh, Let's not overlook the educational aspect of the zoo, where every visit teaches you something new about our planet.
And, believe it or not, even a day at the mall can be educational, showing you the latest in technology, fashion, and design.
There's something magical about watching the sunset at the zoo, as the day slowly comes to an end and the animals settle down.
Finding a quiet corner in the mall to enjoy a coffee and people-watch can be surprisingly relaxing in the midst of chaos.
The excitement of spotting your favorite animal out and about during a zoo visit never gets old, does it?
Stumbling upon a flash sale at your preferred store in the mall feels like hitting the jackpot, right?
Have you ever attended a feeding time or a talk by the zookeepers? It's a great way to learn and engage.
Navigating the mall during holiday seasons is both thrilling and overwhelming with the decorations and the crowds.
The zoo's gift shops are perfect for finding unique gifts that also support wildlife conservation.
Ever notice how the ambiance of a luxury department store in the mall can make you feel like you're in a different world?
There's a sense of community at the zoo, especially when everyone's excited to see a rare animal make an appearance.
The food court in the mall offers a world tour of cuisines, perfect for when you can't decide what you're in the mood for.
Observing the intricate social behaviors of animals at the zoo can be as captivating as watching a drama unfold.
The thrill of discovering a new store opening in the mall brings a fresh wave of excitement for your shopping adventures.
A zoo visit is a gentle reminder of the beauty and diversity of life on Earth, urging us to protect it.
The mall's seasonal displays and events add an extra layer of enjoyment to the shopping experience.
Getting to the zoo right as it opens means you get to enjoy the peace before the crowds arrive.
The satisfaction of finding exactly what you need after a long search in the mall is unmatched.
Zoo exhibits designed to mimic natural habitats offer a window into the world of the animals.
Late-night shopping at the mall, with fewer crowds and more relaxed vibes, can be quite enjoyable.
The interconnected paths of the zoo encourage exploration and discovery, similar to wandering through unfamiliar sections of the mall.
Finally, both the zoo and the mall offer opportunities for learning and growth, be it about wildlife or the latest cultural trends.
So, starting off the day with that first bell- it's like the starter pistol for the race, isn't it? Every class a different lap.
And then there's the rush to the locker between classes, a mini-maze of students all trying to beat the clock.
; Lunchtime is its own adventure, finding your friends in the sea of tables and settling in for stories and snacks.
I've always found the library to be a sanctuary during breaks, a quiet escape from the hustle of the school day.
uh, Group projects can be a mixed bag, right? They're a test of patience and collaboration, but so rewarding when everything clicks.
; Science labs bring out the inner experimenter in all of us, mixing chemicals and peering into microscopes.
The excitement of gym class, where everyone's energy levels just skyrocket- it's contagious, even if sports aren't your thing.
Or how about those moments in art class, where you're free to express whatever's on your mind through paint and pencil?
uh, School assemblies, though sometimes long, can be surprisingly uplifting with the right speakers or performances.
; And let's not forget the school bus ride- its own ecosystem of friendships, rivalries, and last-minute homework.
There's always that one subject that challenges you more than the rest, pushing you to grow and adapt.
Finding your spot in the cafeteria, where the noise somehow blends into a background for your thoughts.
uh, The relief and satisfaction of turning in a project you've worked on for weeks, feeling a weight lift off your shoulders.
; Elective classes offer a taste of freedom, choosing subjects you're genuinely interested in exploring further.
The final bell of the day rings like a liberation anthem, signaling the end of one chapter and the start of whatever comes next.
Walking home or to the bus with friends, rehashing the day's events and laughing over inside jokes.
School plays and concerts, where the community comes together to celebrate the talents of its students.
The rhythm of the school year, with its predictable highs and lows, shaping the narrative of our academic lives.
Participating in school clubs, where passions and interests find a communal ground and friendships are forged.
Homework, though often dreaded, is a quiet companion to the evening, a bridge between school and home life.
Parent-teacher meetings, a crossroads of perspectives, offering insights and forging partnerships in education.
School sports matches, where school spirit ignites and everyone comes together to cheer on their team.
The annual school fair, a highlight of the year, blending fun, fundraising, and community spirit.
Finding a mentor in a teacher, someone who guides, challenges, and inspires you in ways you hadn't expected.
The nervous excitement of presenting in front of the class, a rite of passage in the journey of learning.
The shared experience of field trips, stepping out of the classroom and into the world, where lessons come to life.
Dealing with the inevitable challenges and setbacks, learning resilience and determination along the way.
Celebrating successes, big and small, recognizing the effort and growth behind each achievement.
The evolving landscape of friendships, the heart of the school experience, where bonds are tested and strengthened.
And finally, the anticipation of summer, a well-earned break and the promise of adventures beyond the school gates.
During physics, we marveled at the stars through the telescope, a blend of science and wonder that made the universe feel a bit closer.
In the bustling cafeteria, amidst the chatter and laughter, I shared my latest poem with friends, finding beauty in the fusion of art and daily life.
; The math puzzle competition in the library was a thrilling race against time, where numbers met strategy in a test of wit and teamwork.
; As we cleaned up after the biology lab, discussing the day's shopping plans, it struck me how learning and leisure intertwine, enriching our lives in unexpected ways.

```

</details>