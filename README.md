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
<p>
Take these sentence for example:

<br/>
``` <br/>
The prisoners were in due course transferred to Newgate, to be put upon their trial at the Central Criminal Court. <br/>
They had to handcuff her by force against the most violent resistance, and still she raged and stormed, <br/>
The Secret Service has attempted to perform this function through the activities of its Protective Research Section <br/>
But the affair still remained a profound mystery. No light was thrown upon it till, towards the end of March, 
Yet the public opinion of the whole body seems to have checked dissipation. <br/>
the Presidential limousine arrived at the emergency entrance of the Parkland Hospital at about twelve:thirty-five p.m. <br/>
Oswald was arrested and jailed by the New Orleans Police Department for disturbing the peace, in connection with a street fight which broke out when he was accosted <br/>
gaming of all sorts should be peremptorily forbidden under heavy pains and penalties. <br/>
we have reached into the heart of the problem which is to provide such annual earnings for the lowest paid worker as will meet his minimum needs. <br/>
it had established periodic regular review of the status of four hundred individuals; <br/>
who was one of the first witnesses to alert the police to the Depository as the source of the shots, as has been discussed in chapter three. <br/>
were governed by rules which they themselves had framed, and under which subscriptions were levied <br/>
might have been more alert in the Dallas motorcade if they had retired promptly in Fort Worth. <br/>
. <br/>
. <br/>
. <br/>
100 sentences <br/>
<br/>
``` <br/>

Generate 100 sentences in a similar writing style. Talk about going to the zoo, going to a shopping centre or a mall and a day at the school. Make sure it looks like the text is from a similar speaker. Same conversational style try to match the speaker characteristics as much as you can.
</p>
</details>

<details>
<summary>Generated sentences</summary>
<p>
TThe family, in anticipation of a delightful day, set forth to the zoological gardens, a repository of nature's marvels. <br/>
Upon entering the grand gates of the shopping centre, they were greeted by a cacophony of sounds, each store vying for attention. <br/>
The majestic lion, king of the animal kingdom, lay in repose under the shade of an ancient oak, barely acknowledging the gathered spectators. <br/>
This journey from classroom to zoo to mall taught one vital lesson: learning thrives not just in silence and books but in the lively embrace of the world's vast wonders. <br/>
Children, with eyes wide with wonder, pressed their faces against the glass of the aquarium, mesmerized by the dance of the tropical fish. <br/>
In the food court, a veritable feast was laid out, offering delicacies from the far corners of the earth, each stall a testament to the culinary diversity of mankind. <br/>
The elephant, with its ponderous gait and wise eyes, seemed to carry the wisdom of the ages as it slowly made its way to the watering hole. <br/>
The milliner's shop, with its array of bonnets and hats, seemed a throwback to a time when headwear was a symbol of one's status in society. <br/>
The shrill cries of the monkeys in their enclosure provided a stark contrast to the otherwise serene ambiance of the zoo. <br/>
Bargain hunters thronged the aisles of the clearance sale, each in search of that elusive deal that would mark the day's triumph. <br/>
The giraffes, with their long necks stretching towards the heavens, seemed to be in a world of their own, aloof from the gaze of the onlookers. <br/>
The scent of freshly baked bread from the bakery mingled with the perfume of the florist, creating an olfactory tapestry that enveloped the shoppers. <br/>
The reptile house, with its dimly lit corridors and the silent watchfulness of its inhabitants, evoked a sense of mystery and ancient lore. <br/>
The jeweler, with a craftsman's eye, meticulously arranged the display, each piece a testament to human artistry and the allure of precious stones. <br/>
The peacocks, with their plumage in full display, strutted with an air of vanity, seemingly aware of their unrivaled beauty. <br/>
The bookshop, a haven of tranquility amidst the hustle and bustle, offered the promise of worlds waiting to be discovered within the pages of its tomes. <br/>
The ice cream vendor, with his cart adorned with pictures of frozen delights, became the center of attention as children clamored for a sweet treat. <br/>
The fragrance section of the department store enveloped shoppers in a cloud of scents, each vial containing the essence of dreams and memories. <br/>
The penguins, with their comedic waddle, provided a moment of levity, their antics a reminder of nature's capacity for joy. <br/>
The antique shop, a treasure trove of history's artifacts, invited the curious to delve into the stories of objects left behind by time. <br/>
The butterfly enclosure, a kaleidoscope of color, offered a moment of enchantment as these delicate creatures flitted from flower to flower. <br/>
In the toy shop, generations of toys stood in silent testimony to the changing tides of children's fantasies and the timeless joy of play. <br/>
The zoo's aviary, a symphony of birdcalls, was a reminder of the vastness of nature's palette, each species a unique note in the harmony of life. <br/>
The café, with its promise of refreshment, became a gathering place for weary shoppers, a brief respite in their quest for commerce. <br/>
As the day waned, the families, laden with purchases and memories, made their way home, their hearts full from the day's adventures in the realms of nature and commerce. <br/>
Upon entering the grand gates of the local zoo, one is immediately struck by the cacophony of sounds, a vivid testament to the diversity housed within. <br/>
The majestic lions, in their enclosures, lay with a regal indifference, surveying their kingdom with lazy, half-closed eyes. <br/>
Children, their faces alight with wonder, pressed eagerly against the glass of the reptile house, their breath fogging up the surface. <br/>
It was a marvel to observe the agile monkeys, who, with deft leaps and bounds, seemed to mock the gravity that bound the rest of us earthward. <br/>
The zookeepers, with a patience born of routine, answered the myriad questions posed by curious onlookers, their knowledge deep and detailed. <br/>
Amidst the aviary's dense foliage, the flash of vibrant plumage revealed the presence of exotic birds, their songs a melody of the wild. <br/>
As the afternoon waned, the crowd at the elephant exhibit grew, each visitor eager to witness the gentle giants' graceful movements. <br/>
The chill of the aquarium's halls contrasted sharply with the outdoor warmth, its blue lights casting an otherworldly glow on fascinated faces. <br/>
At the penguin enclosure, the birds' comedic waddle elicited laughter and delight, a welcome relief from the more somber moods of some exhibits. <br/>
The gift shop, strategically placed at the zoo's exit, offered an array of souvenirs, each item a tangible memory of the day's adventures. <br/>
The vast expanse of the shopping center loomed ahead, its many stores promising untold treasures to those willing to explore. <br/>
The hum of conversation filled the air, a constant backdrop to the clatter of shopping carts and the soft shuffle of feet on polished floors. <br/>
In the food court, the mingling aromas of a dozen different cuisines created a tantalizing invitation to dine. <br/>
Sales signs, bold and beckoning, adorned the windows of every shop, each one a siren call to bargain hunters. <br/>
The mall's central atrium, adorned with seasonal decorations, became a gathering place for weary shoppers seeking a moment's rest. <br/>
Teenagers roamed in packs, their laughter echoing off the high ceilings, a hallmark of the freedom found in such communal spaces. <br/>
Parents, their patience stretched thin, navigated the crowds with strollers in tow, their journeys marked by frequent stops and starts. <br/>
The latest fashion trends were on full display, mannequins dressed in the height of style, silently inviting onlookers to update their wardrobes. <br/>
Occasionally, a street performer would captivate an impromptu audience, their artistry adding a layer of unexpected delight to the shopping experience. <br/>
As night fell, the shopping center's lights shimmered like stars, transforming the complex into a beacon for those seeking late-night entertainment. <br/>
The morning's light barely crept through the classroom windows as students shuffled in, the day's lessons a looming presence in their minds. <br/>
In the corridors, the echo of footsteps mingled with the distant sound of a bell, heralding the start of another academic venture. <br/>
The chalk's screech against the blackboard filled the room, each word written by the teacher a testament to the day's learning objectives. <br/>
Students huddled over textbooks, their brows furrowed in concentration, a silent battle against the complexities of new knowledge. <br/>
The library stood as a sanctuary of silence, its shelves laden with the weight of words, a haven for those seeking solace in study. <br/>
Lunchtime brought a cacophony of sounds to the cafeteria, the clatter of trays and the murmur of conversations a welcome interlude. <br/>
On the playground, the air was filled with the shouts and laughter of children, a brief escape from the confines of the classroom. <br/>
Teachers patrolled the halls with a vigilant gaze, their presence a constant reminder of the order that governed the school's daily life. <br/>
In the science lab, the smell of chemicals mingled with the sense of anticipation, each experiment a journey into the unknown. <br/>
Art class revealed a burst of color against the school's otherwise monochrome backdrop, creativity blooming amidst strict schedules. <br/>
The gym echoed with the sound of sneakers on wood, the physical exertion a counterbalance to the day's mental challenges. <br/>
History lessons unfolded like stories, the past coming alive through the teacher's words, a bridge across time. <br/>
Mathematics, with its numbers and equations, offered a puzzle for the mind, logic and reasoning entwined in a dance of digits. <br/>
The school bell's ring, a clarion call, signaled the end of one period and the start of another, a cyclical reminder of time's passage. <br/>
In the computer lab, screens glowed with the promise of technological exploration, fingers dancing over keyboards in digital discovery. <br/>
Language classes wove a tapestry of sounds, the nuances of grammar and vocabulary a challenge to master. <br/>
The school counselor's office offered a haven of advice, a guiding light for those navigating the tumultuous waters of adolescence. <br/>
As the final bell rang, the rush of students towards the exit was a torrent of relief, the promise of home a sweet end to the day. <br/>
Homework assignments, like seeds of knowledge, were planted in the minds of students, destined to grow in the soil of their intellect. <br/>
School buses lined up like sentinels, their engines humming a song of departure, ready to ferry their charges back to the comforts of home. <br/>
Extracurricular activities flourished in the after-school hours, each club and team a microcosm of shared interests and talents. <br/>
The setting sun cast long shadows across the schoolyard, a quiet reminder of the day's end and the passage of another page in the academic year. <br/>
Teachers gathered in the staff room, their conversation a blend of reflection and anticipation, the day's events a mosaic of triumphs and challenges. <br/>
The silence that settled over the empty classrooms was a stark contrast to the day's earlier bustle, a momentary pause in the cycle of education. <br/>
Lost items found their way to the school's lost and found, each one a story of forgetfulness and the hope of reunion. <br/>
The principal's office, often perceived as a place of authority and discipline, also served as the heart of the school's administrative life. <br/>
Bulletin boards, adorned with notices and achievements, offered a snapshot of school life, a collage of opportunities and accolades. <br/>
Parent-teacher meetings, scheduled in the calendar, promised a confluence of perspectives, a partnership in the educational journey. <br/>
The school's garden, tended by student volunteers, bloomed with the seasons, a living lesson in nature's cycles. <br/>
As night descended, the school stood silent and empty, a vessel of dreams and aspirations, waiting to be filled again with the dawn of a new day. <br/>
Early in the morning, the school organized a field trip, a journey that promised both education and entertainment, to the local zoo. <br/>
Students gathered at the entrance, their chatter blending with the distant calls of animals, a prelude to the day's adventures. <br/>
On their way, the bus passed by the city's sprawling shopping center, its vastness a reminder of commerce's reach. <br/>
Upon arrival, the sight of the majestic elephants immediately captivated the students, a living lesson in biology and conservation. <br/>
The teachers, acting as guides, pointed out the importance of each habitat, their words weaving knowledge into the fabric of experience. <br/>
In the reptile house, the students faced their fears, learning that understanding can turn apprehension into respect. <br/>
The gift shop at the zoo offered educational souvenirs, each item a memento of learning outside the classroom walls. <br/>
Meanwhile, a group of students tasked with a project on economics ventured into the shopping center, their observations aimed at understanding consumer behavior. <br/>
They noted the variety of stores, each catering to different needs and wants, a practical lesson in supply and demand. <br/>
The food court provided a study in choices and preferences, a live demonstration of market segmentation and targeting. <br/>
Back at the zoo, a keeper's talk on endangered species sparked a discussion among students about responsibility and environmental stewardship. <br/>
The aquarium's serene beauty offered a moment of reflection, the silent fish a contrast to the bustling corridors of the school. <br/>
As the day drew to a close, the students gathered for a sketching session, capturing the animals' forms, a blend of art and observation. <br/>
Returning to school, they passed the shopping center once more, its lights a beacon in the early evening, a symbol of the community's pulse. <br/>
The bus ride back was a buzz of excited conversations, each student sharing their day's highlight, a chorus of shared experiences. <br/>
Upon their return, the schoolyard, usually a scene of hurried departures, was a place of animated recounting, the field trip a bonding experience. <br/>
Teachers reminded students to pen down their reflections, an assignment that would bridge their experiences with their curricular studies. <br/>
In the following days, presentations were made, the zoo and shopping center visits transformed into educational showcases. <br/>
Students debated the ethics of zoos and the impact of consumerism, their classroom a forum for critical thinking and exchange. <br/>
Art projects inspired by the trip adorned the hallways, turning the school into a gallery of student creativity and insight. <br/>
The economics project group presented their findings, the shopping center's dynamics distilled into graphs and analyses. <br/>
Reflections on the endangered species talk led to a school-wide initiative on sustainability, the field trip sparking action. <br/>
The zoo visit, once merely an outing, became a catalyst for a deeper understanding of biology, ecology, and environmental science. <br/>
The shopping center excursion, too, shed light on the practical applications of mathematics, social studies, and economics. <br/>
As the term progressed, the memories of the field trip lingered, a reminder of the day when the zoo and the mall became classrooms without walls.
</p>
</details>

### Ryan Speech


<details>

<summary>Prompt</summary>
<p>
Take these sentence for example: <br/>
 <br/>
``` <br/>
No, my friends keep me company. <br/>
It grows somewhat like the lily of the valley, but its height is about three feet. <br/>
Do you want to add anything to the order? <br/>
Do you mean you are from England or you speak English? <br/>
Could I be doing something different to make this more enjoyable? <br/>
And could I book those flights for the morning, if possible? <br/>
Even the creatures of the wood knew and loved him, for he never hurt anything that God had made. <br/>
With logs of trees, a few hurdles, and other field appliances, a rustic banqueting hall was prepared and everything was very nice. <br/>
Yes, they are playing at seven ten p m against the Cubs. <br/>
They did not touch me, but merely showed the natural curiosity which is felt at the sight of a foreigner who has appeared unexpectedly. <br/>
From paradise, I think, said Otto, with that patient seriousness that he had caught from the monks, and that sat so quaintly upon him. <br/>
Why does unscented hair spray smell? <br/>
I was at school in Canton Berne; it is a mother tongue to me. <br/>
 <br/>
. <br/>
. <br/>
. <br/>
100 sentences <br/>
``` <br/>
 <br/>
Generate 100 sentences in a similar writing style. Talk about going to the zoo and going to a shopping centre or a mall. Make sure it looks like the text is from a similar speaker
</p>
</details>


<details>

<summary>Generated sentences</summary>
<p>
The lions at the zoo roared loudly, as if they were greeting us personally upon our arrival. <br/>
I couldn't help but marvel at the vibrant colors of the parrots, chatting away in their enclosure. <br/>
Do you think the elephants enjoy painting? I asked, watching one create a beautiful piece with its trunk. <br/>
The smell of fresh popcorn wafted through the air, leading us to the zoo's quaint little snack stand. <br/>
We found a bench by the monkey exhibit, perfect for a quick rest and some people-watching. <br/>
Should we buy a souvenir? I pondered aloud, eyeing the cute stuffed animals in the gift shop. <br/>
The aquarium section was mesmerizing, with its soothing blue lights and the graceful dance of the fish. <br/>
I had to chuckle at the zebras, who seemed to be engaged in their own version of a staring contest with us. <br/>
Look, the new tiger cubs! exclaimed my friend, as we hurried over to the big cat area. <br/>
It was feeding time for the giraffes, and we got to watch them stretch their long necks for lettuce. <br/>
I've always found the reptile house both eerie and fascinating, with its silent, watchful inhabitants. <br/>
The petting zoo was a hit with the children, their laughter mixing with the sounds of the animals. <br/>
I wonder what it's like to be a zookeeper, I mused, watching a worker tend to the flamingos. <br/>
The penguin parade was about to start, a daily highlight that drew a cheerful crowd. <br/>
We paused to admire the orchids in the zoo's tropical greenhouse, a riot of color and fragrance. <br/>
Shall we adopt an animal? the sign suggested, offering a way to support the zoo's conservation efforts. <br/>
As we left, the peacocks bid us farewell, their feathers a stunning display of nature's artistry. <br/>
The mall was bustling, a lively hub of shoppers and diners alike. <br/>
We made a beeline for the bookstore, a treasure trove of stories waiting to be discovered. <br/>
The food court offered a world tour of cuisines, making it hard to choose just one. <br/>
This sale is too good to miss! I overheard someone say, clutching a handful of discounted clothes. <br/>
The new tech store had the latest gadgets on display, drawing a crowd of eager customers. <br/>
I found a cozy corner in the coffee shop, perfect for people-watching and sipping my latte. <br/>
Do you want to try the virtual reality experience? my friend asked, pointing to a new setup near the center. <br/>
The aroma of freshly baked cookies led us to a small bakery, where we couldn't resist buying a dozen. <br/>
We stumbled upon a local artist's pop-up gallery, each piece more captivating than the last. <br/>
The ice skating rink was a whirl of motion, laughter echoing as skaters glided past. <br/>
Let's take a photo in the photo booth, suggested my friend, a fun way to capture our mall adventure. <br/>
The fashion show on the central stage was a dazzle of lights, music, and stunning outfits. <br/>
A group of street performers gathered a crowd, their acrobatic feats leaving everyone in awe. <br/>
I could spend hours in this place, I thought, admiring a shop dedicated entirely to exotic teas. <br/>
The mall's indoor garden was a peaceful retreat, complete with a trickling fountain and benches. <br/>
They have a workshop today on DIY jewelry, my friend noted, interested in the craft event. <br/>
We paused to watch a cooking demonstration, the chef's skills as impressive as the delicious samples. <br/>
Remember to validate your parking, a helpful sign reminded us, a small but important detail. <br/>
The children's play area was a hive of activity, a safe space for little ones to burn off energy. <br/>
Let's check the map, I suggested, realizing just how easy it was to get turned around in the sprawling mall. <br/>
A flash sale at the electronics store caused quite the stir, bargain hunters rushing in. <br/>
The luxury brand section was like stepping into another world, with its opulent displays and exclusive boutiques. <br/>
This place has the best smoothie bar, my friend claimed, leading the way to a hidden gem. <br/>
We signed up for the mall's loyalty program, enticed by the promise of discounts and special offers. <br/>
The seasonal decorations made the mall feel festive, from twinkling lights to oversized ornaments. <br/>
I've been looking for this book everywhere! I exclaimed, finally finding a rare edition in the second-hand. <br/>
The zoo was bustling with families, a true testament to its popularity among locals and tourists alike. <br/>
I couldn't help but admire the elegant flamingos, their pink feathers a stark contrast against the blue pond. <br/>
Isn't it fascinating how the monkeys swing with such ease, almost as if they're performing for an audience? <br/>
Our next stop has to be the lion's den; I've heard their roars can be heard across the entire zoo. <br/>
Do you think the gift shop will have those adorable plush elephants? My niece would love one. <br/>
Walking through the reptile house felt like stepping into another world, each enclosure a window to a different habitat. <br/>
I found myself captivated by the slow, graceful movements of the sea turtles in the aquarium section. <br/>
Would you like to grab a bite at the zoo cafe, or shall we pack our own picnic next time? I pondered aloud. <br/>
The map shows a bird aviary nearby, let's make sure to visit. I've always been intrigued by exotic birds. <br/>
Watching the penguins dive into the water is always a highlight for me; their antics are so playful and amusing. <br/>
Remember to wear comfortable shoes, I reminded my friend, knowing we'd be doing a lot of walking. <br/>
The idea of a guided tour sounds intriguing. Do you think we'll learn more about the animals that way? <br/>
I'm curious about the conservation efforts here. It's important to support zoos that prioritize animal welfare. <br/>
The souvenir shop was our last stop, a chance to bring home a piece of our memorable day. <br/>
As we left the zoo, I felt a renewed sense of wonder for the natural world and its inhabitants. <br/>
Transitioning to our mall adventure, the vibrant store displays immediately caught our eye. <br/>
Do you think the food court has that new sushi place? I asked, already craving something fresh and delicious. <br/>
The shopping center's layout was impressive, with wide aisles and plenty of seating areas for weary shoppers. <br/>
I couldn't resist stopping by the bookstore; there's something about browsing shelves that feels so comforting. <br/>
The mall's indoor garden was a peaceful retreat amid the hustle and bustle of shoppers. <br/>
Let's check out the electronics store for the latest gadgets, suggested my companion, eager for new tech. <br/>
Fashion boutiques lined the corridors, each window more enticing than the last. <br/>
We made a pact to only buy what we needed, but the seasonal sales were too good to pass up. <br/>
The aroma from the bakery was irresistible, leading us to indulge in freshly baked pastries. <br/>
How about a movie after shopping? The cinema's latest offerings promised a perfect end to our day. <br/>
The mall's art exhibit added a cultural touch to our visit, showcasing local talent. <br/>
Finding a parking spot was a challenge, a reminder of the mall's popularity on weekends. <br/>
I heard there's a new virtual reality arcade, my friend mentioned, excitement in their voice. <br/>
We laughed over ice cream cones, sharing stories and making plans for our next outing. <br/>
As we exited the mall, bags in hand, we couldn't help but feel content with our day's discoveries. <br/>
The jewelry store window glinted with promise, tempting us with its sparkling displays. <br/>
Shall we take a break and people-watch for a bit? It's always interesting to observe the mall's diverse crowd. <br/>
The children's play area was alive with laughter, a joyful sight that brought smiles to our faces. <br/>
We stumbled upon a pop-up shop selling handmade goods, a delightful find that supported local artisans. <br/>
The escalators offered a moment of rest, a brief pause as we moved between floors. <br/>
This place has everything, I mused, impressed by the variety of stores and services available. <br/>
The sound of live music led us to a small stage where a local band was performing, adding to the mall's lively atmosphere. <br/>
We made sure to visit the outdoor section of the mall, enjoying the blend of shopping and nature. <br/>
I could spend hours here, my friend said, echoing my thoughts about the mall's inviting environment. <br/>
As the day drew to a close, we reflected on our zoo and mall adventures, grateful for the memories made. <br/>
The morning bell echoed through the halls, signaling the start of another day filled with learning and discovery. <br/>
I hurried to my first class, clutching my notebook and pencil, eager to jot down the day's lessons. <br/>
The chemistry lab was a buzz of activity, with students mixing solutions and marveling at the reactions. <br/>
Do you understand this math problem? I whispered to my classmate, struggling with a particularly tricky equation. <br/>
Our history teacher brought the past to life, weaving tales of ancient civilizations with such passion and detail. <br/>
Lunchtime was a welcome break, a chance to recharge and share stories with friends under the warm sun. <br/>
The library's quiet corners offered a perfect escape for those moments when the world outside felt too loud. <br/>
I lost track of time browsing the shelves, each book a doorway to a different time and place. <br/>
Are you joining the after-school club meeting today? I was asked, reminded of the communities that thrived beyond the classroom. <br/>
The art room smelled of paint and possibility, a space where creativity knew no bounds. <br/>
Our teacher encouraged us to express ourselves freely, reminding us that there's no wrong way to create art. <br/>
The gym echoed with the sounds of bouncing balls and sneakers squeaking against the polished floor. <br/>
I cheered on my classmates during the basketball game, feeling a sense of pride and camaraderie. <br/>
As the afternoon sun cast long shadows, I noticed the beauty of the campus, with its sprawling grounds and ancient trees. <br/>
Homework club is a lifesaver, I thought, grateful for the extra help and the quiet space to study. <br/>
The science fair posters lined the hallway, each project a testament to the curiosity and hard work of my peers. <br/>
What's your project about? I asked, intrigued by the innovative ideas on display.
</p>

</details>


## Spontaneous speech

### Trinity Speech and Gesture Dataset II

<details>

<summary>Prompt</summary>
<p>
 <br />
Take these sentence for example: <br />
 <br />
``` <br />
; , Finish at like six; , or maybe seven or eight; then we'd all go out, you know have a few drinks head out to a nightclub or something like that come home. <br />
; a bit of a; kind of a short story rather than just one scene; So all the class we all got together, the base was because every time we went to a new class. <br />
; , And then all of a sudden the cameras came on and Leonardo DiCaprio was like; Just sitting like this just blocking himself, ; , And we're like oh shit it's Leonardo DiCaprio And then he was literally just like, ; <br />
; for six months, in relation to college, I went over to a place called; , Old Westbury Golf and Country Club in Long Island So I stayed there for six months. <br />
I don't know if he looks at it as a regret, ; But the way he was talking about it you could see he was saddened by it; which kind of was, kind of puts things into perspective for you that like. <br />
We started off in Amsterdam; , So I went to Amsterdam Germany Poland; , Um; , Croatia Slovenia. <br />
people in the music industry, and; But I think I told you the story before but I'm going to tell it again anyway; Oh sorry even a better story than that. <br />
 <br />
. <br />
. <br />
. <br />
total 100 sentences <br />
``` <br />
 <br />
Generate 100 sentences in a similar conversational spontaneous style containing disfluencies, hesitations, repeats etc. With approximately similar lengths. Talk about going to the zoo, going to a shopping centre or a mall and talk about your day at the school.  Here ; is a breath and , is a pause use these too and generate syntactically similar sentences. Make it sound natural as one will do in conersational settings. Use fewer commas and fewer uh and uhm.

</p>

</details>

<details>
  <summary>Generated sentences</summary>
<p> 
<br/>
; I'm like, should we take photos? But my phone, it's dead, completely dead.  <br/>
; And then, the elephants, they're huge, you know? Just massive.  <br/>
; We're walking, and suddenly, this peacock just shows up, fanning its feathers.  <br/>
; I'm trying to get a closer look, but, you know, there's this fence.  <br/>
; Oh, and the gift shop, it was, kind of pricey, but I bought a keychain.  <br/>
; We were starving, so we thought, let's grab a bite, but the line, it was so long.  <br/>
; Then, we're leaving, and it starts to rain, just our luck, right?  <br/>
; I saw this cute hat, but when I tried it on, it looked weird on me.  <br/>
; We saw these kids, running around, screaming ; parents nowhere.  <br/>
; And then, there's the ice cream stand, but I dropped mine, just plop on the ground.  <br/>
; We thought about going to the aquarium section, but it was, like, closed for maintenance.  <br/>
; So, we're at the mall now, and it's packed, I mean, really crowded.  <br/>
; I'm looking for a parking spot, and it's like, there's none, just circles around.  <br/>
; We finally find this one store, and they're having a sale but nothing in my size.  <br/>
; My friend wants to check out this new electronics store, and I'm like, sure, why not?  <br/>
; Then, this guy, he spills his drink, and it's everywhere, on the floor.  <br/>
; We're about to leave, and my friend realizes, she lost her phone.  <br/>
; So, we backtrack, everywhere we went, and finally, it's at the lost and found.  <br/>
; And there's this kiosk, selling these quirky sunglasses, so I get a pair.  <br/>
; We pass by this jewelry store, and there's this beautiful necklace, but, you know, too expensive.  <br/>
; I'm trying on shoes, and this one pair, it's perfect, but the left one's tight.  <br/>
; We're heading out, and there's this group of teenagers, just loud and everywhere.  <br/>
; I remember, I wanted to buy this book, but the bookstore, it's gone, replaced.  <br/>
; We see this advertisement for a movie, and we're like, should we watch it? But we're too tired.  <br/>
; Oh, and the escalators, one of them was broken, so we had to take the stairs.  <br/>
; I'm looking for a restroom, and when I find it, there's a line, of course.  <br/>
; We wanted to sit and relax, but all the benches, they're taken, every single one.  <br/>
; There's this new makeup store, and I'm like, let's just look, ended up buying lipstick.  <br/>
; We're trying to find this specific shop, and we ask for directions, but it's confusing.  <br/>
; And then, there's this sale sign, but when we get there, it ended yesterday.  <br/>
; I wanted to buy a gift, but I'm indecisive, so I left with nothing.  <br/>
; We're leaving the mall, and I realize, I forgot where we parked.  <br/>
; Finally, we find the car, and it's like, we've been walking forever.  <br/>
; So, back to the zoo, remember? There was this funny parrot, mimicking people.  <br/>
; And I'm trying to get a video, but then it just stops, typical.  <br/>
; We're at the reptile house, and it's cool, but kind of creepy, snakes everywhere.  <br/>
; I wanted to see the pandas, but they're asleep, just our luck, again.  <br/>
; We're at this exhibit, and there's supposed to be this rare bird, but we can't find it.  <br/>
; Oh, and the map, it's confusing, we got lost, like, three times.  <br/>
; There's this play area for kids, and it's chaotic, but the kids are having fun.  <br/>
; We're about to watch this feeding show, but it's so crowded, can't see a thing.  <br/>
; And then, we're leaving, and this bird, it poops, nearly misses me.  <br/>
; So, we're hungry, and we find this place, but it's just hot dogs.  <br/>
; And the zoo, it's closing, but we missed the last show, didn't know the time.  <br/>
; We're exiting, and there's this huge line for the tram, so we walk.  <br/>
; Back at the mall, we see this art exhibit, but it's closing in 10 minutes.  <br/>
; There's this store, all about sports, and my friend's excited, but I'm bored.  <br/>
; We try this new coffee place, and it's good, but took forever to get our order.  <br/>
; And there's this contest, win something, but we never win those, didn't bother.  <br/>
; We're looking for a bathroom again, and it's cleaner than I expected, thankfully.  <br/>
; We pass by this pet store, and there are puppies, but we just look, can't have pets.  <br/>
; And then, this store, it's playing loud music, but it's actually pretty good.  <br/>
; We're about to go home, and I realize, I didn't buy what I came for.  <br/>
; So, we're planning to go back, but maybe on a weekday, less people, hopefully.  <br/>
; And that's it, our trip to the zoo and the mall, just a regular day, but fun.  <br/>
; So, like, I get to school, right? And first thing, I forgot my math homework, just left it on the table.  <br/>
; And there's this quiz in history, I'm like, barely awake, trying to remember dates and stuff.  <br/>
; Lunchtime comes, and I'm sitting with my friends, and we're talking about this new game, everyone's obsessed.  <br/>
; Then, in gym class, we're playing dodgeball, and I'm hit, like, immediately, out in the first round.  <br/>
; I'm walking to the next class, and I see this poster for the school play, thinking maybe I should try out.  <br/>
; So, English class, we're reading this book, and I actually like it, but I'm behind a few chapters.  <br/>
; And there's this group project, right? But no one wants to take the lead, so it's kind of awkward.  <br/>
; I'm at my locker, and it won't open, just stuck, and I'm pulling and pulling, finally, it pops open.  <br/>
; Then, there's this assembly, supposed to be motivational, but it's just, you know, kind of boring.  <br/>
; We're leaving the assembly, and everyone's trying to be the first out, just a huge crowd at the doors.  <br/>
; And I'm thinking about the math homework I forgot, wondering if I can make up some excuse.  <br/>
; So, after school, there's practice for the soccer team, and I'm late, sprinting across the field to join.  <br/>
; And we're doing drills, and I'm trying, but I keep messing up, coach is not happy.  <br/>
; Practice ends, and we're all tired, but we decide to go grab something to eat, just hang out.  <br/>
; I'm on my way home, and I realize, I have this huge project due tomorrow, barely started.  <br/>
; So, I'm home, right? And I'm trying to work on this project, but my computer decides to update.  <br/>
; And I'm panicking, watching the update screen, just praying it finishes in time.  <br/>
; Finally, it's done, and I'm typing as fast as I can, but it's like, I can't get my thoughts straight.  <br/>
; I take a break, and I'm just staring out the window, thinking about how much I dislike group projects.  <br/>
; Then, my friend calls, asking about the math homework, and I'm like, forgot it, can you help?  <br/>
; We're on the phone, and she's trying to explain this math problem, but I'm just not getting it.  <br/>
; So, it's getting late, and I'm still not done with the project, feeling stressed.  <br/>
; And then, I remember, I have a science test too, just great, another thing to worry about.  <br/>
; I'm trying to study for science, but all I can think about is how much I want to sleep.  <br/>
; Then, I get a text from my friend, saying we should have studied together, missed opportunity.  <br/>
; It's past midnight, and I'm finally done with the project, but now I need to study.  <br/>
; I'm reading my science notes, and it's like, none of this is staying in my head.  <br/>
; And I think, maybe a quick nap will help, but I'm worried I won't wake up in time.  <br/>
; So, I set multiple alarms, just in case, and lay down, but my mind is racing.  <br/>
; And I'm thinking about the day, all the things that went wrong, and what's waiting for me tomorrow.  <br/>
; Eventually, I fall asleep, but it's not restful, keep waking up, checking the time.  <br/>
; Morning comes, and I'm groggy, trying to remember everything I studied last night.  <br/>
; I'm at breakfast, and I'm not really hungry, just nervous about the test and the project presentation.  <br/>
; And I'm out the door, backpack heavy with books, hoping today will be better than yesterday.  <br/>
; I get to school, and first thing, there's a pop quiz in English, didn't see that coming.  <br/>
; And I'm sitting there, trying to remember what I read, but it's all a blur.  <br/>
; Lunchtime, and I'm with my friends, but I can't stop thinking about the science test.  <br/>
; Then, it's time for the test, and I'm looking at the questions, some of it's familiar, thankfully.  <br/>
; After the test, I'm not sure how I did, just hoping for the best, really.  <br/>
; And then, it's time for the project presentation, and our group is a mess, but we manage.  <br/>
; School's finally over, and I'm walking out, feeling like I've survived a marathon.  <br/>
; I'm on my way home, and I'm thinking, maybe I'll take it easy tonight, just relax.  <br/>
; But then, I remember, I have homework in three subjects, no rest for the weary.  <br/>
; So, I'm home, and I'm starting on homework, but first, a snack, need some energy.  <br/>
; And I'm working, and it's not so bad, feeling a little better about things.
</p>
</details>

### AptSpeech

<details>

<summary>Prompt</summary>
<p>
Take these sentence for example: <br/>
``` <br/>
And you can assume that all of the openings are doorways that will have doors that can open and close- So, <br/>
Yes, and any room can be anything you want it to be. It's really up to you guys to decide how to divide up the space. so that you're comfortable living there. <br/>
so we'd like to talk a little bit about maybe some good or maybe some bad experiences you've had with roommates. <br/>
uh And I will be able to give you advice, because I am a world renowned interior decorator and designer, <br/>
shopping centers starting with bedroom, kitchen, living room bathroom, rugs and miscellaneous. <br/>
uh sharing a space with somebody. ; : Have you had a roommate in your life? : More than one time? : And what about you? Have you had more than, <br/>
; and that subject is, ; roommates, ; or flatmates, or anyone you've ever shared, ; a living space with, ; <br/>
; is we're going to have a conversation just between the three of us, ; and we're going to talk about a particular subject, ; and that subject is, ; roommates, ; <br/>
And any issues uh sharing the like the combined space? Like say the living room, maybe you had a TV or a music system. <br/>
My recommendation would be to start with the bedrooms again because these are bare essentials. Everyone must sleep - at least a few hours a night. <br/>
or exercise or games or - things of that nature so there's plenty of stuff to, use the rooms for. <br/>
; and the reason we find this interesting is because it's a it's a tricky situation. : ; to sharing a space with someone but there can also be, ; <br/>
there's lots of options when you go and look in the- furniture store, you'll see that there's a lot of items in the miscellaneous category, <br/>
. <br/>
. <br/>
. <br/>
100 sentences <br/>
``` <br/>
 <br/>
Generate 100 sentences in a similar writing style. Talk about going to the zoo and going to a shopping centre or a mall. Make sure it looks like the text is from a similar speaker. Same conversational style try to match the speaker characteristics as much as you can. Here ; is breath try to use it wisely. do not over use breathing (;) use it only where it would be appropriate.  Create sentences to train a TTS model so it should not be too long and not too short too something that can be 10-11 seconds.
</p>

</details>

<details>

<summary>Generated sentences</summary>
<p>
So, visiting the zoo is like stepping into a whole new world, isn't it? Each exhibit is a doorway to a different habitat. <br/>
uh, And you know, you can decide to follow the map or just wander. It's really up to you to explore. <br/>
; So we'd like to talk about maybe some memorable or maybe some forgettable experiences you've had at the zoo. <br/>
And I can give you tips, because I've visited zoos all over the globe, from the savannas of Africa to the rainforests of Brazil. <br/>
Then there's the shopping center or mall, starting with the food court, clothing stores, electronics, home goods, and, uh, the miscellaneous shops. <br/>
Sharing a day out with someone at the zoo; have you ever done that? : Once? : More than once? : What about at the mall? Have you gone shopping with, <br/>
; and that's what's interesting, ; zoo visits and shopping trips, ; or any day out where you've shared the experience, <br/>
; we're going to have a chat, just between us, about those experiences, ; and specifically about, ; days out, ; <br/>
Any issues sharing the experience? Like navigating through crowds or deciding where to eat? <br/>
I'd recommend starting your zoo visit with the big attractions, like the lions or elephants. They're the main draws for a reason. <br/>
or maybe you're more into the shopping experience, looking for deals or the perfect outfit. <br/>
; and the reason this is fascinating is because it's a it's a mix of personal tastes and compromises when sharing these experiences, <br/>
There's a lot of options when you hit the mall - you'll see a wide variety in each store, especially in the 'new arrivals' sections, <br/>
you have to ask me- but as you can see, we have many options for spending the day - whether at the zoo or the mall, <br/>
have you ever had an experience, though, with someone who couldn't decide where to eat at the mall, and you just wandered aimlessly? <br/>
The food court can be a battleground, I'd say, because it's a spot everyone has an opinion on. <br/>
okay, well let's talk about those two destinations you just mentioned, the zoo and the mall. <br/>
mhm, sure - that actually leads us nicely into what we're planning next. <br/>
would you trade a zoo visit for a day at the mall? That's a tough choice for some. <br/>
The vibrant colors at the zoo are so natural - whereas the mall lights offer a more artificial ambiance. <br/>
well, considering your preferences might help. Let's see how that influences your choices, huh? <br/>
but remember, whatever you share on social media about your day out, we get to discuss here. <br/>
Yes, you can visit as many stores as you want, but remember, budget constraints mean you can't buy everything you like. : ; <br/>
no issues while exploring together, huh? <br/>
and let's start planning these outings, with some suggestions - so I'm just going to take you through some options. We've got two main destinations: the zoo and the mall. <br/>
I don't think there's a need to rush. Take your time to enjoy each moment. <br/>
And, uh, when you're at the zoo, don't you just love those moments when an animal comes right up to the glass? It's like they're greeting you personally. <br/>
So, how about when you find that perfect spot at the mall, right? The one store where everything just calls out to your style. <br/>
; Let's not forget, the parking situation - at the zoo or the mall - can make or break the start of your day. <br/>
I've got to say, the food options at the zoo have really stepped up; it's not just about snacks anymore but a whole dining experience. <br/>
uh, And if you're at the mall, do you prefer the big department stores or the unique, boutique shops? <br/>
; Planning your route through the zoo can be as strategic as planning your shopping spree to catch all the best sales. <br/>
The energy at the zoo early in the morning is unbeatable, with all the animals just waking up. <br/>
Or the calmness of the mall just as it opens, when the stores are all pristine and the crowds haven't arrived yet. <br/>
uh, Have you ever had that moment at the zoo when the weather just does a complete turnaround? Always brings a sense of adventure. <br/>
; And, talking about weather, the mall is a great escape on those days - endless entertainment without worrying about rain or shine. <br/>
You know, there's always that one exhibit at the zoo that you find yourself returning to, time and again. <br/>
Similarly, there's that one store in the mall that seems to have a magnetic pull, right? <br/>
; I always find it interesting to watch how people interact with the animals at the zoo, those moments of connection. <br/>
And at the mall, it's fascinating to observe the latest trends catching everyone's attention. <br/>
uh, The souvenir shops at the zoo are like treasure troves, each item telling a story of conservation and wonder. <br/>
Just like the specialty stores in the mall, where you can find those one-of-a-kind items that just scream 'you'. <br/>
; Ever noticed how a day at the zoo can make you forget all your worries? It's like a mini-vacation. <br/>
And how a successful shopping trip can give you that sense of accomplishment, like you've conquered the mall. <br/>
uh, Let's not overlook the educational aspect of the zoo, where every visit teaches you something new about our planet. <br/>
And, believe it or not, even a day at the mall can be educational, showing you the latest in technology, fashion, and design. <br/>
There's something magical about watching the sunset at the zoo, as the day slowly comes to an end and the animals settle down. <br/>
Finding a quiet corner in the mall to enjoy a coffee and people-watch can be surprisingly relaxing in the midst of chaos. <br/>
The excitement of spotting your favorite animal out and about during a zoo visit never gets old, does it? <br/>
Stumbling upon a flash sale at your preferred store in the mall feels like hitting the jackpot, right? <br/>
Have you ever attended a feeding time or a talk by the zookeepers? It's a great way to learn and engage. <br/>
Navigating the mall during holiday seasons is both thrilling and overwhelming with the decorations and the crowds. <br/>
The zoo's gift shops are perfect for finding unique gifts that also support wildlife conservation. <br/>
Ever notice how the ambiance of a luxury department store in the mall can make you feel like you're in a different world? <br/>
There's a sense of community at the zoo, especially when everyone's excited to see a rare animal make an appearance. <br/>
The food court in the mall offers a world tour of cuisines, perfect for when you can't decide what you're in the mood for. <br/>
Observing the intricate social behaviors of animals at the zoo can be as captivating as watching a drama unfold. <br/>
The thrill of discovering a new store opening in the mall brings a fresh wave of excitement for your shopping adventures. <br/>
A zoo visit is a gentle reminder of the beauty and diversity of life on Earth, urging us to protect it. <br/>
The mall's seasonal displays and events add an extra layer of enjoyment to the shopping experience. <br/>
Getting to the zoo right as it opens means you get to enjoy the peace before the crowds arrive. <br/>
The satisfaction of finding exactly what you need after a long search in the mall is unmatched. <br/>
Zoo exhibits designed to mimic natural habitats offer a window into the world of the animals. <br/>
Late-night shopping at the mall, with fewer crowds and more relaxed vibes, can be quite enjoyable. <br/>
The interconnected paths of the zoo encourage exploration and discovery, similar to wandering through unfamiliar sections of the mall. <br/>
Finally, both the zoo and the mall offer opportunities for learning and growth, be it about wildlife or the latest cultural trends. <br/>
So, starting off the day with that first bell- it's like the starter pistol for the race, isn't it? Every class a different lap. <br/>
And then there's the rush to the locker between classes, a mini-maze of students all trying to beat the clock. <br/>
; Lunchtime is its own adventure, finding your friends in the sea of tables and settling in for stories and snacks. <br/>
I've always found the library to be a sanctuary during breaks, a quiet escape from the hustle of the school day. <br/>
uh, Group projects can be a mixed bag, right? They're a test of patience and collaboration, but so rewarding when everything clicks. <br/>
; Science labs bring out the inner experimenter in all of us, mixing chemicals and peering into microscopes. <br/>
The excitement of gym class, where everyone's energy levels just skyrocket- it's contagious, even if sports aren't your thing. <br/>
Or how about those moments in art class, where you're free to express whatever's on your mind through paint and pencil? <br/>
uh, School assemblies, though sometimes long, can be surprisingly uplifting with the right speakers or performances. <br/>
; And let's not forget the school bus ride- its own ecosystem of friendships, rivalries, and last-minute homework. <br/>
There's always that one subject that challenges you more than the rest, pushing you to grow and adapt. <br/>
Finding your spot in the cafeteria, where the noise somehow blends into a background for your thoughts. <br/>
uh, The relief and satisfaction of turning in a project you've worked on for weeks, feeling a weight lift off your shoulders. <br/>
; Elective classes offer a taste of freedom, choosing subjects you're genuinely interested in exploring further. <br/>
The final bell of the day rings like a liberation anthem, signaling the end of one chapter and the start of whatever comes next. <br/>
Walking home or to the bus with friends, rehashing the day's events and laughing over inside jokes. <br/>
School plays and concerts, where the community comes together to celebrate the talents of its students. <br/>
The rhythm of the school year, with its predictable highs and lows, shaping the narrative of our academic lives. <br/>
Participating in school clubs, where passions and interests find a communal ground and friendships are forged. <br/>
Homework, though often dreaded, is a quiet companion to the evening, a bridge between school and home life. <br/>
Parent-teacher meetings, a crossroads of perspectives, offering insights and forging partnerships in education. <br/>
School sports matches, where school spirit ignites and everyone comes together to cheer on their team. <br/>
The annual school fair, a highlight of the year, blending fun, fundraising, and community spirit. <br/>
Finding a mentor in a teacher, someone who guides, challenges, and inspires you in ways you hadn't expected. <br/>
The nervous excitement of presenting in front of the class, a rite of passage in the journey of learning. <br/>
The shared experience of field trips, stepping out of the classroom and into the world, where lessons come to life. <br/>
Dealing with the inevitable challenges and setbacks, learning resilience and determination along the way. <br/>
Celebrating successes, big and small, recognizing the effort and growth behind each achievement. <br/>
The evolving landscape of friendships, the heart of the school experience, where bonds are tested and strengthened. <br/>
And finally, the anticipation of summer, a well-earned break and the promise of adventures beyond the school gates. <br/>
During physics, we marveled at the stars through the telescope, a blend of science and wonder that made the universe feel a bit closer. <br/>
In the bustling cafeteria, amidst the chatter and laughter, I shared my latest poem with friends, finding beauty in the fusion of art and daily life. <br/>
; The math puzzle competition in the library was a thrilling race against time, where numbers met strategy in a test of wit and teamwork. <br/>
; As we cleaned up after the biology lab, discussing the day's shopping plans, it struck me how learning and leisure intertwine, enriching our lives in unexpected ways.
</p>
</details>


<script>

function play_audio(filename, condition_name){
      let audio_id = "audio-stimuli-from-listening-test";
      audio = document.getElementById(audio_id);
      audio_source = document.getElementById(audio_id + "-src");
      stimulus_span = document.getElementById(audio_id + "-span");

      audio.pause();
      audio_source.src = filename;
      stimulus_span.innerHTML = condition_name;
      audio.load();
      audio.play();
}
</script>


# Stimuli from the listening test

<p>Currently loaded stimulus: <span id="audio-stimuli-from-listening-test-span" style="font-weight: bold;"> FS2-LJ DET 1</span></p>
<p>Audio player: </p>
<audio id="audio-stimuli-from-listening-test" controls="">
    <source id="audio-stimuli-from-listening-test-src" src="stimuli/FS2/LJ/DET_1.wav" type="audio/wav" />
</audio>

## Fast Speech 2 (FS2)

<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky" colspan=2>LJ</th>
    <th class="tg-0pky" colspan=2>RS</th>
    <th class="tg-0pky" colspan=2>TSGD2</th>
    <th class="tg-0pky" colspan=2>AptS</th>
  </tr>
  <tr>
    <th class="tg-0pky">DET</th>
    <th class="tg-0pky">FM</th>
    <th class="tg-0pky">DET</th>
    <th class="tg-0pky">FM</th>
    <th class="tg-0pky">DET</th>
    <th class="tg-0pky">FM</th>
    <th class="tg-0pky">DET</th>
    <th class="tg-0pky">FM</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/LJ/DET_1.wav', 'FS2-LJ DET 1')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/LJ/FM_1.wav', 'FS2-LJ FM 1')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/RS/DET_1.wav', 'FS2-RS DET 1')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/RS/FM_1.wav', 'FS2-RS FM 1')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/TSGD2/DET_1.wav', 'FS2-TSGD2 DET 1')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/TSGD2/FM_1.wav', 'FS2-TSGD2 FM 1')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/AptS/DET_1.wav', 'FS2-AptS DET 1')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/AptS/FM_1.wav', 'FS2-AptS FM 1')" /> 
      </center>
    </td>
  </tr>
  <tr>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/LJ/DET_2.wav', 'FS2-LJ DET 2')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/LJ/FM_2.wav', 'FS2-LJ FM 2')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/RS/DET_2.wav', 'FS2-RS DET 2')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/RS/FM_2.wav', 'FS2-RS FM 2')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/TSGD2/DET_2.wav', 'FS2-TSGD2 DET 2')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/TSGD2/FM_2.wav', 'FS2-TSGD2 FM 2')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/AptS/DET_2.wav', 'FS2-AptS DET 2')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/AptS/FM_2.wav', 'FS2-AptS FM 2')" /> 
      </center>
    </td>
  </tr>
  <tr>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/LJ/DET_3.wav', 'FS2-LJ DET 3')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/LJ/FM_3.wav', 'FS2-LJ FM 3')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/RS/DET_3.wav', 'FS2-RS DET 3')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/RS/FM_3.wav', 'FS2-RS FM 3')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/TSGD2/DET_3.wav', 'FS2-TSGD2 DET 3')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/TSGD2/FM_3.wav', 'FS2-TSGD2 FM 3')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/AptS/DET_3.wav', 'FS2-AptS DET 3')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/AptS/FM_3.wav', 'FS2-AptS FM 3')" /> 
      </center>
    </td>
  </tr>
  <tr>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/LJ/DET_4.wav', 'FS2-LJ DET 4')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/LJ/FM_4.wav', 'FS2-LJ FM 4')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/RS/DET_4.wav', 'FS2-RS DET 4')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/RS/FM_4.wav', 'FS2-RS FM 4')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/TSGD2/DET_4.wav', 'FS2-TSGD2 DET 4')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/TSGD2/FM_4.wav', 'FS2-TSGD2 FM 4')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/AptS/DET_4.wav', 'FS2-AptS DET 4')" /> 
      </center>
    </td>
    <td>
      <center>
        <img src="play_button_black.png" height="40" style="cursor: pointer;" onclick="play_audio('stimuli/FS2/AptS/FM_4.wav', 'FS2-AptS FM 4')" /> 
      </center>
    </td>
  </tr>
</tbody>
</table>


## VITS


## Matcha-TTS
