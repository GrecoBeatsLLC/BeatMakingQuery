# BeatMakingQuery
Set of code used to automatically create, upload, and distribute trap beats
I am utilizing this readme to give a general overview of how the current code works, so that it can be rebuilt in a way that logically makes sense from an automation standpoint.
Currently this query is designed to run in FL Studio, but DawDreamer is ideal for creating beats in Python

Pt. 1: Sounds
Although this query is fairly autonomous, it requires premade sounds to work properly. At this point, generative AI is not powerful enough to create loops. Instead, services like Splice & online loop kits are very useful, even if royalties need to be split.
Melody loops require a few parts to work: a query that auto trims silence to signify when the loop starts and ends and a way to identify the key and bpm of the loop (i.e., serato sample). Alternatively, BPM can be gathered from the loop's name. This requires some level of manual checking
Drum sounds come from a premade kit, where random number generation is used to select which sound will work. Different genres will require different drum kits, but each beat channel can use the same kit

Pt. 2: Beat Formatting
After identifying the bpm and key of the loop, the project can begin to be formatted. Note: a loop must stay within its gridlines to function properly. If it isn't perfectly cut to its BPM, it will break the project.
Beat arrangement will never be less than 2 minutes, but will always be less than 3.5 minutes
All drum patterns are pre-made via midi. Random number generation is used to select the right drum pattern
All beats are routed through a pre-made mix template, ensuring that all beats are properly leveled in FL studio. Limiters are used on the melody to lock volume in place
808 patterns are premade and tuned based upon the key of the loop

Pt. 3: Video Creation
A query will be provided that automatically makes YouTube videos in Python
The query requires a folder that is full of "Type Beat" style images of the artist. This can be auto downloaded from the internet, the pictures do not matter that much.
All videos must have a 1920x1080 aspect ratio, with a 1080x1080 image in the middle of the video

Pt. 4: Video upload
Hashtags are currently done manually, but stay the same for every beat on a channel. Descriptions follow the same setup
To automate hashtags, grab the hashtags from the top 3 videos in a niche, and then randomly choose between them.
I have not fully automated this process yet, but video upload can be done fully in Python with proper login credentials. Email creation has to be manual.
Store all login credentials in a Google Sheet

Pt. 5: Beatstars upload
Beatstars upload also can be done fully in python
Only 3 hashtags will be used, use generic ones
Beatstar page funding will be handled by Greco Beats LLC, cost per page is $20

