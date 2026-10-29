# Chapter 2: Five Years

In January 2014 I had worked for Schicksal for four years and ten months.

My badge said SENIOR ENGINEER now, under a new photo where my hair was only sticking up a little. I was twenty-two. I still had the same room with the same window looking out at the same concrete wall, because by the time anyone offered me a better one I'd stopped noticing the wall, and moving meant packing. I could run ten kilometers along the seawall without stopping. I'd eaten, by Asami's count, around nine hundred packets of instant noodles. Every spring I sat in the medical room and let a machine sting my arm, and every spring the light on the front of it stopped at F.

I still hadn't been anywhere near Nagazora, and the Third Eruption was a few weeks away.

---

The island was the first thing I worked out, back in the spring of 2009.

It took me about a week. The technical center was built into one end of it, mostly underground, and from the roof of the cafeteria building you could see the rest. It was a flat, man-made island a few kilometers long, with a seawall all the way around, a runway, a harbor, and a lot of empty ground where something was clearly about to be built. Cranes stood around it all spring. Trucks came off ships in the harbor every day.

In June, the something turned out to be a school.

I found out the way everyone else on the eleventh floor did, from a memo. The Far East Branch was getting a new head. She would also be the principal of a new academy for training young Valkyries, to be built on the island, called St. Freya. All departments were asked to support the transition. The memo was signed by an administrator I'd never heard of, and the new head's name was at the top.

Theresa Apocalypse.

I read the memo at my desk four times and then went to the bathroom so I could make a face nobody would see.

I knew this part. In the game, St. Freya was where everything started. Theresa had built it after the Second Eruption, after she found out what had happened to Cecilia, after she fell out with Otto so badly that she couldn't stand to be near him and couldn't leave Schicksal either. The island had been his gift to her. I'd always thought it was a strange gift, and I thought so even more now that I was standing on it.

She arrived at the end of June. I didn't see her arrive. Nobody on the eleventh floor did, because we were underground with no windows, but you could tell something had happened because the cafeteria was suddenly full of people talking about how small she was.

I met her in August.

---

It was a Tuesday, and I was at my desk working through the binder, which by then was down to about two centimeters. Dr. Mori was in his office with the door shut. Somewhere behind me two of the simulation engineers were arguing about the friction value of wet sand.

The door at the far end of the floor banged open, and the whole room went quiet.

She came down the aisle between the desks very fast. She was tiny. I'd known she would be small, but knowing it and seeing it were different. She was about a head and a half shorter than me, with long white hair tied in a low ponytail that hung over one shoulder, and she was wearing a frilly white and blue dress that looked a little like a nun's habit designed by somebody who liked lace. In the game she'd had the face of a twelve-year-old. In person she didn't. She had a grown woman's face, small and sharp-featured, with bright blue eyes, and right then it was furious.

She was carrying a battlesuit gauntlet. It was a training model, white plastic and metal, the kind the first St. Freya students had started wearing in the simulation rooms that summer. The wrist joint was bent at an angle that wrist joints don't bend.

She walked straight past every desk and into Dr. Mori's office without knocking. The sign on his door still said DO NOT KNOCK UNLESS ON FIRE, so technically she was following the rules.

"Principal," I heard Dr. Mori say. He sounded like a man who'd been asleep.

"One of my girls broke her wrist this morning," she said. Her voice was higher than I'd expected and very clear, and she wasn't trying to keep it down. "In your simulation room. In your training suit. The joint locked in the middle of a movement and kept going in the other direction. She's fourteen. Who wrote the code for this?"

There was a pause.

"The actuator module's old," Dr. Mori said. "It was written before any of us got here. We've been..."

"I don't care when it was written. I care that it broke her wrist. Who is responsible for it now?"

Another pause. Then Dr. Mori's head appeared around the door of his office. He looked down the room until he found me, and he looked at me with real apology in his eyes, and he pointed.

The actuator module was in the binder. Of course it was. I'd been working through the binder in order, and it was two-thirds of the way down, in a section of the code that everyone called "Grandma" because it was old and nobody was allowed to touch it. There was a ticket about it, closed in 2008 without a fix, with a note at the bottom. Field incident, see report 2008-117. Subject deceased. I'd read that ticket on my first day.

The principal came out of the office and walked down the room toward me, holding the gauntlet.

"You," she said. "What's your name?"

My heart was going, and my head went clear and quiet. It noticed that she was angry at the right people. It noticed that she wasn't going to shout at me, exactly, but she wasn't going to leave until something got fixed.

"Eros," I said. "The module's on my list. Give me ten minutes."

She stopped. She looked at me for a second, then at the binder open on my desk, and then she pulled the chair over from the empty desk next to mine and sat down in it right beside me, close enough that I could smell something sweet, like sugar.

"Ten minutes," she said. "I'll wait."

I opened Grandma.

I'd read the code before, in the evenings, the way you read the parts of a codebase you're scared of so that you know where the bodies are. It was a mess. The module read the position of each joint from a sensor, decided how much force the motor should apply, and sent the order. Somewhere in the middle, it also read a temperature sensor, because a programmer years ago had worried about the motors overheating. If the temperature went too high, the code cut the force. Fine. But the same programmer had written the check badly, and if the temperature read too low, the number wrapped around and the code thought it was too hot instead. It cut the force on one side of the joint and not the other.

"Is the simulation room cold?" I asked.

"What?"

"In the mornings. Is the room cold?"

She thought about it. "The air conditioning's broken. The girls complain they're freezing until lunch."

"That's it." I turned the monitor a little so she could see, though I didn't expect her to read it. "When the suit's cold, this line thinks it's overheating. It cuts power to the muscle on one side of the joint, and the other side keeps pulling. So the joint goes the wrong way."

She leaned in and looked at the screen, frowning. She read it. I could see her eyes moving along the lines.

"And in the field," she said slowly. "Somewhere cold."

I didn't say anything. She didn't need me to. She looked at the bottom of the ticket, at the note from 2008, and her mouth went thin.

I fixed it. It took four lines. Then I wrote a test that ran the module at every temperature from minus forty to plus sixty and checked that nothing wrapped, and ran it, and everything came back green. Then I pushed it to the training suits and flagged it for the field suits, marked urgent, with Dr. Mori's name on the approval.

It took eleven minutes. She didn't mention the extra one.

"Done," I said. "The training suits will update tonight. The field suits need approval from the Battlesuit Division, but I've flagged it."

"I'll make sure they approve it." She said it in a way that made me believe her. She sat back in the chair and looked at me properly for the first time, up and down, as if I were a new student.

"Eros," she said. "You're the weather data boy."

I blinked.

"Grandfather's people sent me your file when I took over." She waved a hand as though she was waving away a fly. "I don't read files from HQ anymore. But people talk." She stood up, which didn't make her much taller than me sitting down, and put her hand in the pocket of her dress, and came out with a wrapped sweet. She put it on my desk next to the keyboard.

"The World's Cutest Valkyrie says thank you," she said. "You may tell people."

Then she picked up her broken gauntlet and walked out of the room as fast as she'd come in, and the door at the far end banged shut behind her.

The whole floor was looking at me. After a moment they all went back to their screens, very slowly, the way people do when they want you to know they weren't watching.

Dr. Mori came out of his office and stood next to my desk. He looked at the sweet. He looked at me.

"You just met the principal," he said.

"Yes."

"Try not to do it again." He went back into his office and shut the door, and I heard the cot creak.

I sat there for a while with the sweet in front of me. It was a strawberry hard candy in pink plastic wrap. I didn't eat it. I put it in my desk drawer, and for the rest of the afternoon I typed with my face very carefully arranged, while inside my head I was shouting so loudly that I'm surprised nobody heard it. I'd sat next to Theresa Apocalypse. She'd sat next to me and read my code over my shoulder and smelled of sugar. And she wasn't twelve. In the game she'd been stuck at twelve forever, and here she was a small grown woman with a temper. It was the first time I'd found something in this world that didn't match the game, and I spent a long time that night lying awake trying to decide what it meant.

---

In 2010 the Valkyrie Assault Squad went out on a mission and almost none of them came back.

I didn't know anyone in it. I read about it the way everyone at the technical center read about everything, in a report that came down to the eleventh floor a week later because some of the dead had been wearing suits running our firmware. My job was to check whether our code had failed. I checked the logs three times. It hadn't. They'd died because what they were sent to fight was stronger than what they'd been told, and no amount of code was going to fix that.

At the bottom of the report was a short list of survivors. One of them was Murata Himeko.

I knew that name too. I sat with the report open in front of me for a long time, and then I closed it and went for a run on the seawall in the rain.

---

The running had started in the first autumn.

I knew what was coming, and I knew what I was. I'd seen the light stop at F. Men didn't become Valkyries, and the rare ones who could handle Honkai energy were born with it, not trained into it. No amount of exercise was going to let me stand in the middle of the Third Eruption and walk out again. But I had died once already at a desk with a numb arm, and I'd decided on my first night here that if I ever had to run away from something, I wanted to be able to run for a long time.

So I ran. At six every morning before work, out of the technical center and along the top of the seawall, with the sea on one side and the half-built school on the other. The first time I made it two kilometers and threw up. By the next spring I could do five. By 2012 I could do ten, and I'd started going to the gym in the basement of the residential block, where the Valkyries in training lifted weights that I couldn't have moved with a forklift.

Asami thought this was the funniest thing she'd ever seen.

"You know you're still going to be F," she told me in the gym once, watching me struggle with a bar that one of the fifteen-year-old trainees had warmed up with. "You could bench press a car and the machine would still say F."

"I'm not trying to change the letter."

"Then what are you doing?"

"Being able to run away."

She considered this. "That's actually smart," she said, and then she put another plate on my bar while I wasn't looking.

She'd become a friend, mostly by accident. She was the only person on the island I'd met before I got there, and she seemed to think that made me partly her responsibility. Once a month or so she dragged me to the bar by the harbor that the logistics crews drank in, and I drank one beer for every three of hers and listened to her complain about helicopter maintenance schedules. She was still D-rank. She'd been offered C twice and turned it down both times, because C meant combat support, and combat support meant being closer to the things on the files.

"I've seen what comes back," she said once, a long way into the evening. "I fly them back. I'm fine where I am."

---

Brenner came to see me once a year.

It was always in March, close to the anniversary of the night he'd waited in my room, and it was always the same. He'd appear at my desk in the same gray suit and ask if I had time for a coffee, and we'd go up to the cafeteria and sit by the window, and he'd ask me questions. How I was finding the work. Whether I had any concerns. Whether anyone had approached me about anything unusual. He had a folder, and he never opened it in front of me.

The first year he asked, out of nowhere, "Why did you say yes so quickly?"

I'd been waiting a year for somebody to ask me that.

"You were offering me the most interesting job in the world," I said. "And the other option sounded bad."

He looked at me over his peppermint. "Most people want to know what the job is before they decide it's interesting."

"I'd just found out the world had a secret that was killing people and that governments were covering it up. I knew it was interesting."

He nodded slowly and didn't write anything down, and I couldn't tell if that was good or bad.

The fourth year, in March 2013, he put down his cup and said, "You know, Eros, you're very boring."

"Thank you," I said.

He almost smiled. I'd known him four years, and that was the closest I ever saw him come.

---

The work changed, slowly.

I finished the binder in my first year. Dr. Mori gave me another one, thinner. Then, in 2010, he called me into his office and asked whether the thing I'd built to find Schicksal in the first place could be rebuilt using Schicksal's own sensors instead of public data.

It could. It took me eight months. By the end of 2011, the Far East Branch's anomaly watch, the system that sat in a room on the ninth floor with a wall of screens and told the duty officers where Honkai energy was rising, ran on my code. It was weird_stuff_v3 with a bigger budget and better data. I didn't tell anyone that's what I called it in my head. In 2012 they made me a senior engineer, and Dr. Mori bought me a coffee from the machine and said, "Don't let it go to your head," and then fell asleep in his chair.

In 2012 an Emperor-class Honkai beast came out of nowhere in India. Two A-rank Valkyries died, and twelve more were badly hurt. The data came in to us afterward in a flood, every reading anybody had managed to take before their equipment broke, and Dr. Mori's team spent three months building a simulation of it for training. It was called Ganesha. I wrote the code for its movement, all those tons of armored body turning and charging and stamping, and while I was writing it I kept thinking about the game, where years from now a training simulation on this same island would glitch and spawn a Ganesha in an exam where it had no business being.

Dr. Mori locked the Ganesha data to the A-rank training set, and I didn't touch the lock.

---

In the autumn of 2013 I looked up Raiden Mei.

I'd told myself for four years that I wouldn't. I had a plan, and the plan was to be boring and somewhere else. Looking her up was not boring. But the anomaly watch was mine, and Nagazora was on it like every other city in the region, and when you spend your whole working life watching numbers you start to wonder about the people behind them.

I didn't use anything from Schicksal. I did it the way I'd done it at seventeen, from public data. A regional high school kendo tournament in the spring. Third place, girls' individual, Raiden Mei, third year, a high school in the Chiba district of Nagazora. A local newspaper's list of top exam results. Raiden Industries' annual report, with a photograph of her father on the second page.

Third year. Born in 1995.

In the game, the girls had been younger when the Third Eruption happened. Kiana and Mei and Bronya had all been born around 2000. I was sure of that, as sure as I was of anything about the story. Here, Mei was eighteen. I went looking for the others and couldn't find them in public records, which made sense, because Kiana and Bronya had never lived the kind of lives that end up in newspapers. But I found enough, in the margins of other things, to guess that it was the same for all of them.

So it was Theresa's face, and now this. The world matched the game in almost everything that mattered, in every date and name and event I'd been able to check. But it had its own ages for some people, and its own faces, and I didn't know how many other small things were different that I hadn't found yet. I took the folded timeline out of my wallet and added a line to it, a function with a name that sounded like a database migration, and I didn't sleep well for a week.

---

In December the readings in Nagazora started to climb.

It was small at first. Little spikes that came and went, the same sharp shape I'd found in the seismic data at seventeen, but tiny, a hundredth of the size of Siberia. The anomaly watch flagged them, because I'd built it to flag them. The duty officers put Nagazora on the watch list, and a note went up the chain, and nothing happened, because spikes that size happened somewhere in the region every few weeks and almost always went away.

These didn't go away. Through December and into January they kept coming, a little bigger each time.

I knew what it was. Somewhere in Nagazora, a girl in her third year of high school who had come third in a kendo tournament was carrying something inside her that was starting to wake up. In a few weeks it would wake up properly, and the city would come apart.

I didn't tell anyone. I thought about it every night, lying in bed looking at the ceiling. I could have walked into Dr. Mori's office or the duty officer's room and said, that city is about to be hit by the worst Honkai event since Siberia. And they would have asked me how I knew. The anomaly watch already told them everything the data could tell them. Anything I added would have to come from somewhere, and the only place it could come from was a game on a different planet. I thought about the portrait of the man in white and gold in the corridor downstairs, and the folder Brenner never opened in front of me. It wasn't a difficult decision. I made it in about a minute and spent the next three weeks feeling sick about how easy it had been.

---

The night it changed was the fourteenth of January.

My phone rang at ten past two in the morning. I was awake already. I'd been awake on and off for weeks.

"Core's doing something," Dr. Mori said. He didn't say hello. "Get down here."

I went down in my running clothes with a jacket over the top. The three security doors were all propped open. In the basement the fans were roaring louder than I'd ever heard them, and there was an alarm going somewhere, a slow two-tone beep, and a red light turning on the ceiling.

The core was wrong. The thing inside the glass cylinder, the slow white light that I'd looked at maybe a hundred times in five years and that had never once done anything but drift, was churning. It folded and refolded on itself fast, too fast, and there was color in it now, something deep and bruised underneath the white. The hum had gone up into a whine that I could feel in my back teeth. Dr. Mori stood at the railing with his tablet, his reading glasses pushed up into his hair, typing with both thumbs.

"Load's spiking and the regulator can't keep up," he said, without looking at me. "I need to reset the regulator by hand, and the reset needs a biometric hold on the panel for the whole cycle. Thirty seconds. Mine's not working, my hands are too dry or something, I don't know. Yours is registered."

My phone buzzed in my pocket. I looked at it. It was an alert from the anomaly watch, which I'd set to message me directly about one city only.

Nagazora. A spike, the biggest yet, at two-oh-eight in the morning. The same minute the core had started churning.

"Eros," Dr. Mori said. "Hand on the panel. Now, please."

I put my hand on the panel.

The jolt was the same as my first day, except that it didn't stop. It went up through my palm and my elbow and my shoulder and into the back of my head, and it stayed there, hard and bright, and kept getting brighter. My teeth were clenched so tight my jaw hurt. Dr. Mori was counting down from thirty under his breath. The light in the cylinder flared, white and that other color together, so bright I had to squint, and the whine climbed and climbed.

Then I heard a voice inside my head.

[Ding!]

[Honkai energy threshold reached.]

[Imaginary Simulation System... binding.]

[Binding complete.]

[Hello, Host.]

"...three, two, one," Dr. Mori said. "Okay. Okay, you can let go."

I let go. The light in the cylinder was already settling, sinking back down into slow white folds. The whine dropped to the old hum. Somewhere the alarm stopped beeping. Dr. Mori let out a long breath and leaned on the railing with both arms.

"You okay?" he said. "It give you a shock?"

"Static," I said.

"Does that." He rubbed his face with both hands. "Go back to bed. Come in at ten. I'll tell the morning shift."

---

I went back to my room and locked the door. I sat on the end of the bed and looked at the concrete wall outside the window.

I'd touched that panel on my first day, nearly five years ago. I'd felt the same jolt and seen the same flicker, and then nothing had happened, and I'd gone on with my life. Tonight I'd heard a voice. I'd also been sleeping badly for weeks, I'd just had a bolt of Honkai energy go through my head, and I'd spent five years wanting something like this to happen. If I was ever going to imagine a voice, tonight was the night for it.

Then I said, out loud, "Hello?"

[Hello, Host.]

It came from inside my head, but not in my own voice. It was soft and even and polite. I couldn't tell if it was a man's voice or a woman's. It sounded like someone who was very happy to see me.

I sat there with my heart going.

"Why didn't you say anything else?" I asked. "In the basement."

[You weren't alone, Host.]

"Mori was looking at a tablet."

[He was still there, Host.]

That was fair.

"What are you?"

[I am the Imaginary Simulation System. I'm here to help you, Host.]

"Help me do what?"

[Grow stronger.]

A panel slid open in front of my eyes. It hung in my vision like a floater does, but crisp and clear and easy to read, with a thin pale border.

```
[Status]
Name: Eros
Age: 22
Combat Rating: Civilian
Honkai Adaptability: F
Soul: Whole
Gifts: None
Fate Fragments: 0
```

I read it three times.

"Civilian," I said.

[Yes, Host.]

"And F."

[Yes, Host.]

Five springs in a row I'd sat in the medical room and watched a light stop at F, and now my own magical System had looked at me and agreed with the machine.

"Okay," I said. "Okay. Tell me how it works."

I asked the questions I'd have asked about any new piece of software, in order, and the System answered every single one of them. It was the best documentation I'd ever read. It never got impatient, it never said "that's out of scope," and it never told me to read the manual.

It ran simulations. I would go into them when I slept. My body would stay here in bed, and one simulation would take about one night of real time, however long it lasted inside. There were normal simulations, which were whole lives, and when I died in one, it ended. When it ended, I'd be graded, and I'd get to choose rewards. Gifts, which were traits I could keep. Skills and knowledge from the life I'd lived. Sometimes items, which I could actually bring out with me. There was a currency called Fate Fragments that I could spend in a shop. I'd be able to do one normal simulation a day for free.

"Can my Adaptability go up?" I asked.

[Some rewards can raise it, Host.]

"Which ones?"

[You'll see when they're offered.]

"Can I get stronger? Physically? In real life?"

[Yes, Host. That's what I'm for.]

I lay back on the bed. I had to, for a minute. I lay there with my arm over my eyes and grinned at the inside of my elbow like an idiot.

Then I sat up again, because something had been bothering me since the basement.

"Imaginary," I said. "Imaginary Simulation System. Why imaginary?"

There was something in this world called the Imaginary Tree. It was the thing that held every possible version of the world, every branch, every timeline. Every lore video I'd ever watched had a section on it. A System with "Imaginary" in its name, that had turned on when I touched a machine that ran on Honkai energy, was not something I was going to let slide.

[It's only a name, Host.]

"Is it connected to the Imaginary Tree?"

[It's only a name, Host.]

I waited. It didn't say anything else.

"Okay," I said. "Then here's a more important one. These simulations. Are they real?"

[No, Host.]

"If I do something in there. If I hurt someone, or someone dies because of me. Is that a real person?"

[No, Host. The simulations are not real. Nothing you do inside them can hurt anyone. ♪]

My shoulders came down. That had been the thing sitting at the bottom of my stomach since the basement. I'd read a lot of web novels in my first life. I knew how systems like this could go.

"Okay," I said. "Good. Okay."

[There are also heroine simulations,] the System added. [They'll unlock when the conditions are met.]

I stopped.

"Heroine simulations," I said.

[Yes, Host.]

"What's a heroine simulation?"

[They'll unlock when the conditions are met.]

"What conditions?"

[You'll see when they unlock, Host.]

I lay back down. I stared at the ceiling. There was a crack in the plaster running from the light fitting to the corner, and I followed it with my eyes, and I was smiling so hard my face hurt.

I knew what kind of stories had systems in them. I'd read hundreds. And this was Honkai Impact, the game I'd spent eight years of my first life playing in every spare minute, usually on my second monitor while something compiled, and it had a lot of heroines. In my first life, in the privacy of my own head, I'd had some very detailed opinions about which of them I'd want to meet. I'd never told anyone, because there'd never been anyone to tell. And in this world, I'd found out that autumn, they were older than I remembered.

Some time later, when my face had calmed down, I asked the last question. I asked it quietly, because I wasn't sure I wanted the answer.

"Did you bring me here?"

[I don't understand the question, Host.]

"Here. This world. Did you put me here? Did you write my name on a piece of paper and leave me at a gate?"

[I don't understand the question, Host.]

I took my wallet out of my back pocket and slid the note out from behind my old student card, past the folded timeline. I unfolded it and looked at it under the lamp. The handwriting was neat and practiced, written by someone who'd spent a lot of their life writing. One word. Eros. I looked at it for a long time, and the System didn't say anything at all. Then I folded the note and put it back.

[Host,] the System said, in the same pleasant voice as before, as though nothing had happened. [You have an unclaimed starter pack.]

"Open it."

[Ding!]

[Starter pack claimed.]

[Free first simulation: 1.]

[Free gift reroll: 1.]

[Fate Fragments: +100.]

[Begin first simulation? Yes / No]

The words sat in the middle of my vision, waiting.

I looked at the clock on the desk. It was nearly three in the morning. Dr. Mori had told me to come in at ten, and I'd known him long enough to know that meant nine. I picked up my phone and set an alarm for six, because I always ran at six. Then I took my shoes off, got under the blanket, turned off the lamp, and pressed Yes.

---

There was no falling, and no tunnel of light. I closed my eyes in my bed, and when I opened them again I was standing somewhere dark and empty with no floor that I could see, and I could feel that I was standing on something anyway.

[Simulation loading.]

[Drawing gifts.]

Five cards appeared in front of me in a row, the size of playing cards, glowing softly. Four of them had white borders. One had a green border.

```
[Light Sleeper (White)]
Wakes at the smallest change in sound, light or vibration.

[Iron Stomach (White)]
Can eat almost anything without getting sick.

[Steady Hands (White)]
Hands don't shake during fine work, even under stress.

[Cold Tolerance (White)]
Handles cold far better than a normal person.

[Quick Learner (Green)]
Picks up skills and languages about twice as fast.
```

[Choose 2 to keep for this simulation. You may use your free reroll.]

I stood in the dark and looked at the cards, and for the first time since the basement, I felt completely at home.

This was the part I was good at. Five options, two picks, incomplete information. I didn't know the scenario yet. That was the main thing. In every game I'd ever played that worked like this, the smart move was to take what would help no matter where you ended up, because a gift that was perfect for one scenario was useless in nine others.

Quick Learner was easy. It was the only green, and it helped with everything. Whatever I was going to be doing in there, I'd learn it twice as fast.

The second one took longer. Iron Stomach was nice but small. Steady Hands would help with fine work, and I was probably going to end up doing some kind of fine work, because that was the job I had. Cold Tolerance was very specific. Light Sleeper was the one I kept coming back to. In a world with Honkai in it, the person who woke up first when something went wrong was the person who got the head start, and a head start was worth more than steady hands.

I looked at the reroll for a while too. The cards were mostly white. A reroll might give me something better. It might also give me five whites. And this was my first simulation, the free one, the tutorial. You don't spend your only reroll on the tutorial.

"Quick Learner," I said. "And Light Sleeper."

The other three cards faded out.

[Gifts locked: Quick Learner (Green), Light Sleeper (White).]

[Scenario: Schicksal maintenance technician. Siberian Branch, Outpost 7. March 1999.]

I read it twice.

Siberia. March 1999. I knew what happened in Siberia less than a year after that, and so did everyone who had ever played the game for more than a week.

I'd also just thrown away Cold Tolerance.

[Simulation begins.]

---

The cold hit me before anything else.

I was sitting in the back of an open truck on a bench, with my knees against a crate of spare parts, and the air was so cold it felt solid. It went straight through my coat and my sweater and my shirt and settled in my bones, and my face was so numb I couldn't tell if my mouth was open. The truck was crawling along a road made of packed snow between two walls of black pine trees. The sky was the color of dishwater.

I had a body. It was me, my own body at twenty-two, fitter than I'd been at eighteen after five years on the seawall, and still not built for any of this. I had a bag between my feet, and in the inside pocket of my coat there was a folded set of papers. Without reading them, I knew what they said. I was a technician on a two-year contract, hired from a Chinese company that did work for Schicksal, and I spoke enough Russian to read a manual and not much more. The simulation had given me all of it, the way you know things in a dream without being told.

The truck came out of the trees and I saw Outpost 7.

It was six prefab buildings and a radio mast in the middle of a field of snow, surrounded by a fence that wouldn't have stopped a determined goat. There were two big fuel tanks, a generator shed with smoke coming out of a pipe in the roof, and a wooden sign by the gate with a number on it and the Schicksal cross painted underneath, faded almost to nothing. Beyond the outpost the land went on flat and white to the north until it met the sky. Somewhere up there, forty kilometers away, was the research city. Nobody at the outpost ever called it anything else.

[1999, March. You arrive at Outpost 7. It is colder than the file said.]

The commander's office was the warmest room in the place, which wasn't saying much. Major Anna Sorokina sat behind a metal desk in a full uniform buttoned all the way to her throat, a tall, thin woman with gray hair pinned flat to her head. She read my papers without looking at me once.

"Your contract is two years, Technician," she said in Russian, and then repeated it slowly when she saw my face. "Two years. You will report to Lebedev. Dismissed."

Lebedev turned out to be the biggest man I had ever seen in either of my lives. He was waiting for me outside the generator shed, in a padded coat and a fur hat with earflaps that he hadn't tied, and his beard was gray and white and frozen solid at the tips. He looked at me, and then at my boots, which were the best boots I'd been able to buy in Hangzhou, and then he started laughing.

"No," he said. "No, no, no."

He went into the shed and came back out with a pair of thick gray felt boots, the kind that come up to your knee, and pushed them into my arms.

"Felt boots," he said. He said it slowly and loudly, the way people talk to foreigners and small children. "Not those city things. You want to keep your toes?"

I nodded.

"Then felt boots." He clapped me on the shoulder hard enough to move me sideways. "Grisha," he said, pointing at himself. Then he pointed at me. "Boy."

[1999, March. Grisha Lebedev gives you a pair of felt boots. Your toes survive.]

---

The simulation didn't make me live every minute. Most of the days went by in a kind of fog, the way the weeks of a long project go by when you look back at them, and while they were going by, lines of text slid across the edge of my vision and told me what had happened. Then something would happen that mattered, and I'd be completely there again, cold and awake and real.

[1999, April. You fix the number two generator. Nobody thanks you.]

[1999, April. You fix the number two generator again.]

[1999, May. Your Russian improves quickly. (Quick Learner)]

[1999, May. Grisha starts calling you "professor" after you fix the radio by reading the manual.]

[1999, June. You hear about "the special project" at the research city for the first time. Nobody knows what it is. Everybody has a theory.]

The theories were mostly stupid. Grisha thought it was a new kind of tank. The cook thought it was aliens. One of the radio operators had heard from a truck driver who'd heard from a guard that there were children there, a lot of them, and that the trucks that went north at night had their windows covered so you couldn't see who was inside.

I listened to all of it and kept my mouth shut. I knew roughly what the research city was doing, and I knew roughly how it ended, and I didn't know nearly as much as I wanted to. The game had given me the shape of it in cutscenes and flashbacks, years after the fact. I knew it happened early in 2000. I didn't know the day.

In July I tried to leave.

I'd thought about it for weeks. This was a normal simulation, and the System had told me how normal simulations were graded. The longer I lived, the better. Staying at Outpost 7 into the new year was the worst possible plan for living a long time.

Major Sorokina read my transfer request in about four seconds.

"Request denied," she said. "Next."

"Major, I..."

"Your contract is two years, Technician. You will serve two years." She looked up at me for the first time since I'd arrived. Her eyes were very tired. "There are no transfers from this outpost. There are no transfers from any outpost in this region. Do you understand?"

I said I understood.

[1999, July. You request a transfer. Major Sorokina denies it.]

[1999, August. Trucks go north to the research city at night. Their windows are covered.]

[1999, September. Grisha teaches you to drive the snowmobile. You crash it twice.]

[1999, October. The first snow that stays.]

[1999, November. You stop being able to feel your feet outside for more than an hour, felt boots or not. You think about Cold Tolerance a lot.]

---

On the last night of 1999, the whole outpost got drunk.

All eleven of us crowded into the mess hall, which was the only room big enough. Someone had found a small plastic Christmas tree and put it on the table with a string of lights that worked about half the time. The cook made something with potatoes and something else with more potatoes. There was vodka, a lot of it, and a radio playing music from Moscow that kept dropping into static. Major Sorokina came in for exactly one drink, raised her glass to the room without a word, and left.

At midnight everybody shouted and hugged and kissed each other on both cheeks, and Grisha picked me up off the ground in a bear hug and put me down again and poured me a glass I didn't want.

"The year 2000!" he roared. "The end of the world! All the computers will explode!"

"They won't," I said.

"How do you know, professor?"

"I just know."

He thought this was the funniest thing anyone had ever said. Later, when the others had started singing, he sat down heavily on the bench next to me and took out his wallet and showed me a photograph, which he'd already shown me four times since March. It was a woman with a kind round face and a teenage girl in a school uniform, squinting in sunlight, standing in front of an apartment block in Novosibirsk.

"Next year she finishes school," he said. "She wants to be a doctor. Can you imagine? A doctor. My daughter."

"Grisha," I said.

"Mm."

I'd had two glasses by then, and it made it easier to say. "Take leave. Now, in January, as soon as you can. Go home to them for a few weeks."

He laughed. "Leave! From here? You've met the major."

"Ask her anyway. Say your wife is sick. Say anything."

He looked at me, and the laughter went out of his face for a moment, and he looked like what he was, a big tired man who'd been working at places like this for twenty years.

"You think the end of the world is coming, boy?" he said. "Here, it comes every winter." He clapped me on the back. "Drink."

I told myself it wasn't real. I told myself that several times that night, sitting on the bench in the mess hall while eleven people who didn't exist sang badly over a radio full of static. It helped a little.

[2000, January. The computers do not explode. The coffee machine breaks. Grisha blames you.]

[2000, January. Grisha asks the major for two weeks' leave. She denies it. He tells you about it as a joke.]

[2000, January. You start a stash behind the fuel drums in the snowmobile shed. Two jerry cans of fuel. Tinned food. A map. A compass. Matches.]

[2000, February. The research city asks for two extra generators. You and Grisha drive them north. You are not allowed past the outer gate.]

I remembered that one. It was the closest I got. The research city was a gray wall three stories high in the middle of the snow, with guard towers on it and lights that stayed on during the day. Behind the wall I could see the tops of buildings, one of them much taller than the rest, with no windows on its upper floors. The guards at the gate took the generators off our truck with a forklift and signed for them and told us to leave, and we left. Grisha didn't say anything on the drive back, which wasn't like him.

[2000, February. Radio traffic from the research city doubles.]

[2000, February. Radio traffic from the research city stops almost completely. The officers say it's equipment trouble.]

---

Light Sleeper woke me up.

I didn't know what had done it. I was just awake, all at once, lying in my bunk in the dark with my heart beating fast. The clock on the wall said a few minutes past three in the morning. Across the room, the other technicians were asleep. Somebody was snoring.

The glass of water on the shelf next to my bunk was shivering. Little rings were moving across the surface, over and over, and I could hear the glass making a faint high sound against the shelf.

I could feel it too, now that I was paying attention. A hum coming up through the floor and into the frame of the bunk. It was very low, too low to hear properly, the same kind of hum I'd felt in the basement of the Far East Branch, standing in front of a cylinder full of light, almost a year ago and also a few hours ago.

I got up and went to the window.

The sky to the north was wrong.

Above the horizon, where the research city was, there was a glow. Fire would have been orange and moving. This was pale and steady, and it lit up the underside of the clouds from below, and while I was looking at it, the clouds above the glow started to pull back from a single point in a ring, smooth and fast, exactly like the satellite images on my laptop in Hangzhou.

In the middle of the ring, where the clouds had been, there should have been stars.

There was nothing. It was a hole, perfectly black, with edges that shimmered and folded over themselves. Looking at it made my eyes water and my stomach turn over. I'd seen things like it drawn and animated in the game a dozen times, and none of them had made me want to throw up.

---

The siren started a minute later, and after that, everything happened fast.

The lights came on. The other technicians fell out of their bunks swearing. Somebody was shouting in the corridor. The radio in the hallway was full of voices, too many at once, crackling and overlapping, and the only words I could pick out were "all units" and "the city" and a lot of screaming numbers I didn't understand. Major Sorokina's voice came over the speakers telling everyone to muster in the yard in full gear.

I put on my coat and my felt boots and my hat, and instead of going to the yard, I went to the snowmobile shed.

Grisha was already there. Of course he was. He'd seen me go out and followed me, and now he stood in the doorway of the shed with the light behind him, looking at me dragging the jerry cans out from behind the fuel drums.

"Professor," he said. "What are you doing?"

"Leaving. You should come."

"The major said muster."

"Grisha. Look at the sky."

He looked at it. He looked at it for a long time. In the light from the north, his face was the color of paper.

Behind him, the radio in the shed crackled. A voice came through, a woman's voice, very fast, half drowned in static. She was calling for vehicles. Any vehicles. There were people coming out of the research city on foot, she said, and they needed trucks on the north road, now, anybody who could hear this.

Grisha turned his head toward the radio.

"There are people," he said.

"I know."

"On foot. In this." He looked at the truck parked by the fuel tanks, the big one we'd driven the generators north in. "Somebody has to go."

"Grisha, don't."

He looked back at me, and I could see that he'd already decided, and that he'd probably decided before he'd finished hearing the message.

"Get the sled going, professor," he said. "Go south. Get to the railhead." He took his fur hat off, looked at it, and pushed it down onto my head over my own hat, so that it came down over my eyebrows. "Tie the flaps. I never do. You should."

Then he went to the truck. I stood in the doorway of the shed with his hat on my head and watched him climb into the cab and start the engine and turn the headlights on, and drive out through the gate and north up the road toward the hole in the sky. Two other men ran after him and jumped onto the back. I watched the taillights until they were small.

Then I loaded the snowmobile and went south.

---

I'd been driving for about ten minutes when I saw them.

At first they were just shapes moving over the snow off to my left, low and fast, and I thought they were birds. Then I saw how big they were. Each one was the size of a person, and there were dozens of them, flying in a loose crowd a few meters above the ground on long wings with edges like blades. They had black armor instead of feathers, smooth and overlapping, with cold blue light shining through the joints. Where a face should have been there was a smooth plate with light behind it. One of them turned that plate toward the sound of my engine for a second, then turned away.

Baradiel. The ice version of the little flying Archangel types, the ones the game always threw at you in crowds. One of the collection entries said they'd been everywhere in Siberia during the Second Eruption. I'd killed thousands of them on my second monitor, between builds, while I argued on forums and ate dinner.

They weren't coming for me. They were flying north, toward the outpost.

The radio on my belt was still on. Through the static, I heard the outpost. The siren was going in the background. Somebody was shouting orders. Then somebody started shooting, short bursts, and then a lot of people were shooting, and then somebody was screaming, a man's voice, high and terrible and going on and on, and then the screaming stopped and the shooting was less.

I kept driving. My hands on the handlebars were shaking so badly that the snowmobile wobbled. My body wanted to stop, or turn around, or curl up in the snow and hide. My head was perfectly clear. South, it said. The railhead was eighty kilometers. I had fuel for a hundred and twenty. If I kept going, the beasts would be busy with the outpost.

The radio clicked over to another channel by itself, the way they did sometimes when one channel went dead. I heard an engine, very loud, and over the engine a big voice I knew, shouting in Russian.

"...on the north road, four kilometers out, we have people, I can see them, there are, there must be thirty, forty..."

There was a noise I didn't recognize. A deep heavy noise, like something enormous landing.

"...what is that? What is..."

The channel went to static, and I kept driving.

---

The thing that killed me came from the right, out of the trees.

It was much bigger than the flying ones, the size of a car, a heavy four-legged thing that moved like a bull with its head down. Its whole body was covered in black plates that overlapped like armor, with cold blue light leaking out between them. It had horns, or something like horns, two of them curving forward, and steam was pouring off its back into the cold air.

A Frost Chariot. Chariots were the most common Honkai beast in the game, slow and heavy, and the frost kind only turned up in cold places. I knew its animation and its attack pattern. It was slow right up until it charged. In the game, you dodged sideways right before it reached you, and then it ran past and you hit it in the back.

I swerved. The snowmobile skidded on a drift and came up on one side and threw me off.

I hit the snow hard. Something in my chest cracked, I felt it go, a sharp, wet pop on the left side, and then I couldn't breathe properly. Every breath was short and caught on something. I rolled over. The snowmobile was on its side five meters away with its engine screaming and its headlight pointing at the trees.

The Chariot had gone past. It was turning around. It turned slowly, like a truck turning in a narrow street, and its head came around toward me.

I tried to get up and couldn't. I got to my hands and knees. The snow was in my mouth and my nose and down the neck of my coat. Grisha's hat had come off and was lying next to my hand.

The air tasted wrong. It tasted of metal, of the smell of a battery when you touch it to your tongue, and every breath I took burned a little more going in. My skin was tingling all over, under my clothes, the same buzzing heat as the Adaptability test, but everywhere, and getting stronger. My eyes were watering. When I wiped them, there was blood on the back of my glove.

Honkai energy. I was breathing it. A body graded F, breathing the air next to a Honkai beast in the middle of an eruption.

Far away to the north, behind the Chariot, under the hole in the sky, there was light moving. Little flashes of it, very bright, very fast, moving against the black. Something up there was fighting. I couldn't see what. I knew how that night ended for almost everyone under that sky, and I knelt in the snow with blood on my glove and watched the little lights move, because it was the only thing I could think of to do.

The Chariot lowered its head. I didn't dodge. My body was too broken to dodge. I watched it come across the snow toward me, the steam on its back and the light between its plates and the snow flying up from its feet, and my head stayed clear right up to the end. It noticed that there was frost on the tips of the horns. It noticed that the thing was much faster when it charged than it had ever looked in the game. The last thing it noticed was Grisha's hat lying in the snow next to my hand, with the flaps still untied.

The horns hit me in the chest and lifted me off the ground, and I felt everything inside me give way at once. I was still looking at the lights in the north when it all went out.

---

[Simulation ended.]

I was in the dark place again, the one with no floor. I was standing up. My chest didn't hurt. I put my hand on it anyway, and it was whole, and I stood there with my hand on my chest and couldn't stop shaking.

[Cause of death: Frost Chariot (Chariot-class Honkai beast). Honkai energy exposure.]

[Soul damage: one whole memory.]

When the line appeared, I felt something. It was small and quick, a little tug somewhere at the back of my head, like someone had pulled a thread out of a sweater. And then it was gone, and I couldn't tell what had been taken.

I went looking. I went through everything I could think of as fast as I could. Director Zhou's face. Her voice saying "bowls." Professor Han's sweater vest. The office on the last night, the energy drinks, Dennis's code. The delivery driver. My first apartment. The way to the bus stop from Willow Street. The cards I'd just picked. Grisha's photograph of his wife and daughter. Everything was there. Everything I looked for was there, and something wasn't, and I didn't know what it was.

"What did I lose?" I asked.

[It will be returned when you wake, Host. Your soul is a little frayed. It will heal in a few days. ♪]

"But what was it?"

[It will be returned when you wake, Host.]

[Settling simulation.]

```
[Simulation 1: Schicksal maintenance technician]
Survived until: the Second Eruption
Hidden event: Witnessed the Second Eruption
Grade: C
```

[Choose 1 of 3.]

Three cards appeared.

```
[Gift: Quick Learner (Green)]
Keep this gift permanently.

[Experience: Field Maintenance (Cold Weather)]
A year of keeping engines and generators alive in a Siberian winter.

[Item: Technician's Multitool (White)]
A sturdy Schicksal-issue multitool.
```

[Fate Fragments: +40.]

I looked at the cards for a long time. My hands had stopped shaking, mostly.

The experience would make me good at my job. Battlesuits were machines, and somebody who'd kept generators running at forty below would understand them faster than somebody who hadn't. The multitool was a joke. I didn't need a multitool.

Quick Learner, though, would make me better at everything, forever. Every skill I ever got from any simulation, every language, every lesson, I'd pick up in half the time. The experience package was a year of work. Quick Learner was all the years after it.

"Quick Learner," I said.

[Quick Learner (Green) added to permanent gifts.]

```
[Status]
Name: Eros
Age: 22
Combat Rating: Civilian
Honkai Adaptability: F
Soul: Frayed
Gifts: Quick Learner (Green)
Fate Fragments: 140
```

[Well done, Host. Waking now.]

---

My alarm went off at six.

I was lying in the bed in my room at the Far East Branch, with the blanket twisted around my legs and the sheet under me soaked through with sweat. The room was warm. I was freezing. I lay there with my phone buzzing on the desk and my teeth chattering and couldn't make my arm move to turn it off.

When I finally did, I sat up, and my chest hurt on the left side, a sharp pain where the rib had gone. I pulled my shirt up and looked. There was nothing there. The skin was smooth and pale and normal. I pressed on it. It didn't hurt when I pressed on it. It only hurt when I didn't think about it.

I went to the bathroom and threw up in the sink.

Then I stood there holding on to the edges of it, looking at myself in the mirror. My face was gray. My eyes were red. I looked like I'd been awake for most of a year, which I suppose I had.

The memory had come back. I could tell, because I knew what it was now. It was the night I'd learned to ride a bicycle, when I was about ten, in my first life. A neighbor had held the back of the seat and run behind me and let go without telling me. It was a small memory. I hadn't thought about it in twenty years.

[Good morning, Host,] the System said, warm and pleased. [Remember, none of that was real. ♪]

"I know," I said to the mirror.

I kept saying it to myself while I brushed my teeth. Grisha didn't exist. Major Sorokina didn't exist. Outpost 7 didn't exist, and nobody in its mess hall had sung along to a radio full of static, and nobody had driven a truck north into the dark because a woman on the radio said there were people on the road.

I knew that the Second Eruption had been real, though. In this world, fourteen years ago, it had happened. I had sat on the floor of the common room at Willow Street with a bowl of sunflower seeds and watched the smoke on the news, and the newsreader had said there were no figures yet on casualties, and I'd laughed and gone to wash the dishes.

I got in the shower and turned it up as hot as it would go and stood under it until the hot water ran out.

At half past seven I went up to the eleventh floor, a long time before anyone expected me. The office was mostly empty. Dr. Mori's door was open, and he was asleep on the cot with his shoes still on and his glasses still pushed up into his hair, and his third monitor was showing a crash log, scrolling slowly. I went to my workstation, sat down, and opened the anomaly watch's feed for Nagazora. The numbers had dropped back after the spike at two-oh-eight, but not as far as they'd been the day before.
