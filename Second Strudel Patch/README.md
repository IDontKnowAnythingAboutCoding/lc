Second Strudel Patch by David Gao
- 

### Code

stack(
  note("<[c3,c2] [ab1,ab2] [f1,f2] [g1,g2]>").euclid(10,16).sound("sine").gain(1.5),
  note("c4 [eb4,bb3] d4 eb4 [eb4,g4]").mask("<1 [0 0 0 0 1]>").sound("gm_music_box").delay(0.4).gain(1.2),
  n("[3 2 ~ ~ 0 0 ~ 6 ~ ~ 6 ~ ~ 4 ~ 2]").scale("C4:minor").palindrome().sound("gm_voice_oohs").delay(0.2),
  ("[KorgKRZ_bd ~ ~ KorgMinipops_bd] [ ~ ~ KorgKRZ_bd KorgKRZ_bd] [~ bd KorgKRZ_bd ~] [~ KorgMinipops_sd KorgMinipops_sd KorgMinipops_sd KorgMinipops_sd ~]").s().gain(0.7), 
  ("[~ ~ ~ ~] [LinnDrum_cp ~ ~ ~] [~ ~ ~ ~] [LinnDrum_cp ~ LinnDrum_cp LinnDrum_cp]").s().gain(0.6).delay("0.1"),
  ("[~ KorgMinipops_hh KorgMinipops_hh ~ KorgMinipops_hh ~ KorgMinipops_hh KorgMinipops_hh KorgMinipops_hh] [KorgMinipops_hh ~ KorgMinipops_hh ~] [ KorgMinipops_hh ~ ~ ~ ] [ ~ KorgMinipops_hh KorgMinipops_hh KorgMinipops_hh ]").s().gain(0.85),
).cpm(30).room(0.15)


### Comments

- Use of reverb & delay

- Use of built-in functions such as *play one per cycle*, *scale* and *palindrome*

- Gain staging

- Attempts to combine elements of different rhythms
