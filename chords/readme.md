#Spec

The goal of this spec is to simplify manually building up a library of chord voicings that can be used for reference or automatic indentification. As such we want a textual format that is easy to enter and visually verify correctness. We want to define transposible voicings once, in their lowest position, then have the computer do the work for us. 
  
1. There will be one chord definition per non comment/all whitespace line.
2. Chord lines will be broken up into 4 sections, in the following order
	* A section that indicates which fret on which string 
	* A section that indicates which suggests which finger to use on which string.
	* The root of the chord
	* The type of chord
3. The fret section uses x to indicate the string is not struck, 0 to indicate an unfretted string is struck, and 1 to 9 to indicate frets 1 through 9. In order to keep the spec simple and encourage authoring chords in the lowest position we will not start out supporting frets greater than 9 (although we probably would by using a ! for the 1). 
4. The finger section uses x to indicate a unused string, 1 for pointer, 2 for middle, 3 for ring, 4 for pinky, and T for thumb. 
5. The chord definition assumes standard tuning. In the future we may allow a directive at the top of a file that indicates all the voicings in this file use this tuning.
6. Sections are seperated by one space.

Example - standard C Major open chord
032010 x32x1x C maj
 
