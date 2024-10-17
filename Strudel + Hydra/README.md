Strudel + Hydra Performance by David Gao
- 
###Code

await initHydra()

src(s0)
noise(1, 1)
  .modulate(noise(4))
  // .modulateRepeat(osc(10), 3.0, 3.0, 0.5, 0.5)
.out(o0)

stack(

sound("BossDR55_bd")
.struct("[x ~ ~ ~] [x ~ ~ ~] [x ~ ~ ~] [x ~ ~ ~]").gain(1.3),
  
note("<[c2 c3]*4 [ab1 ab2]*4 [f2 f3]*4 [g1 g2]*4>") 
  .lpf("200 300 400 200")
  .sound("gm_synth_bass_2"),
  
  
n("[1 2 0 ~ 0 ~ 1 4 ~ ~ 3 ~ ~ 4 2 1]").scale("C4:minor").gain(0.7).palindrome().sound("gm_fx_crystal").delay(0.2),
  
sound("KorgMinipops_sd")
  .struct("[~ ~ ~ ~] [x ~ ~ ~] [~ ~ ~ ~] [x ~ x x]").gain(0.5),
sound("LinnDrum_cp")
  .struct("[~ ~ ~ ~] [x ~ ~ ~] [~ ~ ~ ~] [x ~ x x]").gain(0.1).delay(0.1),
sound("hh*8")
  .bank("RolandTR909")
  .gain(0.1)
  .degradeBy(0.33)
  .gain(0.4),
  
note("<c4 f3 bb3 d4>")
  .euclidLegato(3,8)
  .sound("sine")
  .fm(1) 
  .gain(0.5).delay(0.1),
  
).cpm(30).room(0.1)


###Comments

- Using *.struct* to form a more unified overall structure 

- Using *.delay* and *.euclidLegato* to create interesting rhythmic elements

- Transitions using functions such as *.gain* and *.lpf*