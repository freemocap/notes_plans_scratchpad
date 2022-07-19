# This is a running list of notes from Twitch streams

https://twitch.tv/freemocap

---
## 2022-07-19 - Twitch Notes

[![hackmd-github-sync-badge](https://hackmd.io/P87BYoOEQ2GPs5li1bx2kQ/badge)](https://hackmd.io/P87BYoOEQ2GPs5li1bx2kQ)


- Hurray I did this lol

here's another coment

here's an unclear thing I wrote

### slap dash notes/worklist of blender stuff

- something something cgtinker/blendARmocap addon (specifically the `freemocap` branch)
     - need to clean up so it, ya know, like works and stuff
         - currently some buggos with the hands and think the feet?
     - need use lessons learned there to automate standard `freemocap` -> blender output so outputted `.blend` is compatible with `rigify`'s standard human metarig
     - soemthing something paolo acompora's addon
         - that connects rigify stuff to mixamo et al I think? 
     - I think the buggos with the BlendAR read in are fixable, but also kinda arise from the current "all data in a giant 3-dimensional numpy array"
         - so I think maybe rather than fixing those buggos directly, we should alter and update the data output format to avoid those kinds of easy-to-make mistakes
             - and also be consistent with `pandas` dataframes 
                 - lead to human readable `csv`'s
                 - which will fit in nicely with @roalddahl (?)'s `tidyMocap` R package (linked to in server)
             - in general prolly gonna wanna use a `dictionary-like` format (or `dataclass`) that separates data from the body, hands, and face
                 - b/c I think many many buggos have arisen from mistakes in indexing into the giant everything numpy array to try to pull out, say, the left hand data
                     - (the main buggo in the BlendAR integration is that one hand is flipped and the other isn't tracked at all kinda)
- Also, we should be checking out/using `makehuman` (says @marcusllewellyn and also someone on the discord server already did something like this, i think it was NordicViking or something? In response to maybe V4NDLO?)
    - http://www.makehumancommunity.org/
