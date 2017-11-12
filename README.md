# NLP - Probablistic Context Free Grammar

This is an assignment inspired by the Stanford assignment for context free grammar. In this assignment  we are required to create grammar that will parse the sentences given to us. These sentences are contained in the file dev.sen

### dev.sen
- Arthur is the king .
- Arthur rides the horse near the castle .
- Arthur rides the plodding horse near the castle .
- the Holy Grail is a chalice .
- the sensational Holy Grail is a sacred chalice .
- every coconut was carried to the hottest mountains .
- sixty strangers are at the Round Table .
- Sir Lancelot might have spoken .
- Guinevere had been riding with Patsy for five weary nights .
- Sir Bedevere might have been suggesting this quest .
- the Britons migrate south frequently .
- Arthur and Guinevere ride frequently near the castle .
- he suggests to grow fruit at home .
- riding to Camelot is not hard .
- do coconuts speak ?
- why does England have a king ?
#challenge
- do not speak again !
- Arthur rode to Camelot and drank from his chalice .

To run the parser
```
python S2generator.py > S2.gr
java -jar pcfg.jar parse -t dev.sen *.gr
```
1st command ensures that there is a generic parse tree available using the file S2.gr.
The grammar written by us is contained in S1.gr.

The objective is to ensure that in the output all the parse trees are from S1.gr(our grammar file) and not from S2.gr.
The final output is as follows:
```
[PCFGParser]	log prob = -29.61	sentence : Arthur is the king .
[PCFGParser]	best parse tree: 
(START
   (S1
      (@NP-VP
         (NP
            (Proper Arthur))
         (VP
            (VerbT is)
            (NP
               (Det the)
               (Nbar
                  (Noun king))))) .))
[PCFGParser]	log prob = -52.22	sentence : Arthur rides the horse near the castle .
[PCFGParser]	best parse tree: 
(START
   (S1
      (@NP-VP
         (NP
            (Proper Arthur))
         (VP
            (VerbT rides)
            (NP
               (NP
                  (Det the)
                  (Nbar
                     (Noun horse)))
               (PP
                  (Prep near)
                  (NP
                     (Det the)
                     (Nbar
                        (Noun castle))))))) .))
[PCFGParser]	log prob = -57.22	sentence : Arthur rides the plodding horse near the castle .
[PCFGParser]	best parse tree: 
(START
   (S1
      (@NP-VP
         (NP
            (Proper Arthur))
         (VP
            (VerbT rides)
            (NP
               (NP
                  (@Det-Adj
                     (Det the)
                     (Adj plodding))
                  (Nbar
                     (Noun horse)))
               (PP
                  (Prep near)
                  (NP
                     (Det the)
                     (Nbar
                        (Noun castle))))))) .))
[PCFGParser]	log prob = -33.41	sentence : the Holy Grail is a chalice .
[PCFGParser]	best parse tree: 
(START
   (S1
      (@NP-VP
         (NP
            (Det the)
            (Nbar
               (NNP Holy) Grail)))
         (VP
            (VerbT is)
            (NP
               (Det a)
               (Nbar
                  (Noun chalice))))) .))
[PCFGParser]	log prob = -43.41	sentence : the sensational Holy Grail is a sacred chalice .
[PCFGParser]	best parse tree: 
(START
   (S1
      (@NP-VP
         (NP
            (@Det-Adj
               (Det the)
               (Adj sensational))
            (Nbar
               (NNP Holy) Grail)))
         (VP
            (VerbT is)
            (NP
               (@Det-Adj
                  (Det a)
                  (Adj sacred))
               (Nbar
                  (Noun chalice))))) .))
[PCFGParser]	log prob = -43.71	sentence : every coconut was carried to the hottest mountains .
[PCFGParser]	best parse tree: 
(START
   (S1
      (@NP-VP
         (NP
            (Det every)
            (Nbar
               (Noun coconut)))
         (VP
            (VBD was)
            (VP
               (VBD carried)
               (PP
                  (TO to)
                  (NP
                     (@Det-AdjS
                        (Det the)
                        (AdjS hottest))
                     (Nbar
                        (Nouns mountains))))))) .))
[PCFGParser]	log prob = -35.22	sentence : sixty strangers are at the Round Table .
[PCFGParser]	best parse tree: 
(START
   (S1
      (@NP-VP
         (NP
            (Number sixty)
            (Nouns strangers))
         (VP
            (VBP are)
            (PP
               (Prep at)
               (NP
                  (Det the)
                  (Nbar
                     (NNP Round) Table)))))) .))
[PCFGParser]	log prob = -27.71	sentence : Sir Lancelot might have spoken .
[PCFGParser]	best parse tree: 
(START
   (S1
      (@NP-VP
         (NP
            (Proper Sir) Lancelot))
         (VP
            (MD might)
            (VP
               (VB have)
               (VP
                  (VBN spoken))))) .))
[PCFGParser]	log prob = -68.36	sentence : Guinevere had been riding with Patsy for five weary nights .
[PCFGParser]	best parse tree: 
(START
   (S1
      (@NP-VP
         (NP
            (Proper Guinevere))
         (VP
            (VBN had)
            (VP
               (VBN been)
               (VP
                  (VBG riding)
                  (PP
                     (Prep with)
                     (NP
                        (NP
                           (Proper Patsy))
                        (PP
                           (Prep for)
                           (NP
                              (Number five)
                              (NP
                                 (Adj weary)
                                 (Nbar
                                    (Nouns nights))))))))))) .))
[PCFGParser]	log prob = -46.69	sentence : Sir Bedevere might have been suggesting this quest .
[PCFGParser]	best parse tree: 
(START
   (S1
      (@NP-VP
         (NP
            (Proper Sir) Bedevere))
         (VP
            (MD might)
            (VP
               (VB have)
               (VP
                  (VBN been)
                  (VP
                     (VBG suggesting)
                     (NP
                        (Det this)
                        (Nbar
                           (Noun quest)))))))) .))
[PCFGParser]	log prob = -27.47	sentence : the Britons migrate south frequently .
[PCFGParser]	best parse tree: 
(START
   (S1
      (@NP-VP
         (NP
            (Det the)
            (Nbar
               (NNPS Britons)))
         (VP
            (VB migrate)
            (ADVP
               (ADV south)
               (ADV frequently)))) .))
[PCFGParser]	log prob = -42.29	sentence : Arthur and Guinevere ride frequently near the castle .
[PCFGParser]	best parse tree: 
(START
   (S1
      (@NP-VP
         (NP
            (@Proper-CC
               (Proper Arthur)
               (CC and))
            (Proper Guinevere))
         (VP
            (@VBP-ADVP
               (VBP ride)
               (ADVP
                  (ADV frequently)))
            (PP
               (Prep near)
               (NP
                  (Det the)
                  (Nbar
                     (Noun castle)))))) .))
[PCFGParser]	log prob = -48.14	sentence : he suggests to grow fruit at home .
[PCFGParser]	best parse tree: 
(START
   (S1
      (@NP-VP
         (NP
            (Pro he))
         (VP
            (VBS suggests)
            (S1
               (VP
                  (TO to)
                  (VP
                     (@VB-NP
                        (VB grow)
                        (NP
                           (Noun fruit)))
                     (PP
                        (Prep at)
                        (NP
                           (Noun home)))))))) .))
[PCFGParser]	log prob = -35.02	sentence : riding to Camelot is not hard .
[PCFGParser]	best parse tree: 
(START
   (S1
      (@S1-VP
         (S1
            (VP
               (VBG riding)
               (PP
                  (TO to)
                  (NP
                     (Nbar
                        (NNP Camelot))))))
         (VP
            (@VerbT-ADV
               (VerbT is)
               (ADV not))
            (ADJP
               (Adj hard)))) .))
[PCFGParser]	log prob = -20.25	sentence : do coconuts speak ?
[PCFGParser]	best parse tree: 
(START
   (S1
      (@@Aux-NP-VP
         (@Aux-NP
            (Aux do)
            (NP
               (Nouns coconuts)))
         (VP
            (VB speak)))
      (. ?)))
[PCFGParser]	log prob = -36.37	sentence : why does England have a king ?
[PCFGParser]	best parse tree: 
(START
   (S1
      (@WHVP-S1
         (WHVP
            (WRB why))
         (S1
            (@Aux-NP
               (Aux does)
               (NP
                  (Nbar
                     (NNP England))))
            (VP
               (VB have)
               (NP
                  (Det a)
                  (Nbar
                     (Noun king))))))
      (. ?)))
[PCFGParser]	found invalid word: '#challenge' in sentence: #challenge
[PCFGParser]	log prob = -21.51	sentence : do not speak again !
[PCFGParser]	best parse tree: 
(START
   (S1
      (VP
         (@Aux-ADV
            (Aux do)
            (ADV not))
         (VP
            (VB speak)
            (ADVP
               (ADV again))))
      (. !)))
[PCFGParser]	log prob = -51.42	sentence : Arthur rode to Camelot and drank from his chalice .
[PCFGParser]	best parse tree: 
(START
   (S1
      (@NP-VP
         (NP
            (Proper Arthur))
         (VP
            (@VP-CC
               (VP
                  (VBD rode)
                  (PP
                     (TO to)
                     (NP
                        (Nbar
                           (NNP Camelot)))))
               (CC and))
            (VP
               (VBD drank)
               (PP
                  (Prep from)
                  (NP
                     (PPro his)
                     (Noun chalice)))))) .))
[PCFGParser]	cross-entropy=5.256 perplexity=3.821e+01
```

PROJECT LICENSE

This assignment was submitted by Ayesha Ahmad as part of the NLP class at Syracuse University.


Me, the author of the project, allow you to check the code as a reference.
Copyright (c) 2017 Ayesha Ahmad

Besides the above notice, the following license applies and this license notice
must be included in all works derived from this project.

MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
