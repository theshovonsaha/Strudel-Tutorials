//First Sound
// Your first beat - press Ctrl+Enter to play!

// SOUNDS: kick drum bd , snare sd , kick drum bd , snare sd (4/4 beat)
// $: sound("bd sd bd sd")


// Mute everything - hush() 
// $: sound("bd sd bd sd")


// Key Commands
// Ctrl+Enter - Play/Update pattern
// Ctrl+. - Stop all sounds


//setcps(0.5) - Set cycles per second (tempo: 0.5 = 120 BPM)
// $: setcps(0.4)
// $: sound("bd sd bd sd")





// Music Theory Essentials {#music-theory}

// ** Scales & Notes ** //
// SOUNDS: Ascending major scale (happy, bright)
// C Major Scale: C D E F G A B C
// 1|2 |3|4 |5|6|7 |8|9 |10|11|12|13
// c|c#|d|d#|e|f|f#|g|g#|a |a#|b |c
// 1 3 4 5 7 
// c d e f g
// $: note("c d e f g a b c5").s("piano")

// Lets build a scale -> 
// E Major Scale: C D E F G A B C
// 1|2 |3|4 |5|6|7 |8|9 |10|11|12|13
// c|c#|d|d#|e|f|f#|g|g#|a |a#|b |c

// SOUNDS: Minor scale (sad, dark, emotional)
// C Minor Scale: C D Eb F G Ab Bb C
// $: note("c d eb f g ab bb c5").s("piano")



// SOUNDS: Simple, folk-like, can't play wrong notes
// Pentatonic (5 notes - sounds good anywhere!)
// $: note("c d e g a").s("piano")


// ** Chords (Multiple Notes Together) ** //

// SOUNDS: Bright, happy C major chord
// Major chord (happy): Root + Major 3rd + Perfect 5th
// $: note("c").s("piano")
// $: note("e").s("piano")
// $: note("g").s("piano")

// SOUNDS: Dark, sad C minor chord
// Minor chord (sad): Root + Minor 3rd + Perfect 5th  
// $: note("c").s("piano")
// $: note("eb").s("piano")
// $: note("g").s("piano")

// SOUNDS: Jazzy, sophisticated sound
// 7th chord (jazzy): Add the 7th note
// $: note("c").s("piano")
// $: note("e").s("piano")
// $: note("g").s("piano")
// $: note("bb").s("piano")


// ** Chords (Multiple Notes Together) ** //
// Strudel can generate chords automatically!
// SOUNDS: Cycles through different chord types
// C major -> A minor7 -> F suspended4 -> E major7
// $: note("c a f e").chord("<major minor7 sus4 major7>").s("piano")


// ** Rhythm Basics ** //
// SOUNDS: Kick on beat 1, silence on 2, 3, 4
// Quarter notes (4 beats)
// $: sound("bd ~ ~ ~")

// SOUNDS: Fast kick-kick-snare-snare
// Eighth notes (8 beats)
// $: sound("bd bd sd sd")

// SOUNDS: Rapid kick rolls then snare rolls
// Sixteenth notes (16 beats - very fast!)
// sound("[bd bd bd bd] [sd sd sd sd]")
// 0=tonic, 2=3rd, 4=5th, 5=6th in major
// n("0 0 0 2 4 5")
//   .scale("<C:major G:major D:major A:major E:major>")
//   .octave(4)         // bring it into a comfy register
//   .s("piano")
//   .slow(5)
//   .gain(0.6)




// setcps(80/120)

// stack(
//   // Drums
//   sound("bd*4"),
  
//   // Chord progression
//   note("d e g a").chord("<major minor7 sus4 major7>").s("piano").gain(0.5),
  
//   // Melody: pentatonic scale
//   note("0 2 4 5 7").scale("<c:major a:minor f:major e:minor>")
//     .s("sine").gain(0.6).slow(4)
// )

// note("c").s("piano")
// note("eb").s("piano")
// note("g").s("piano")
