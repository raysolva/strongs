# overview

This is raw draft overview based on an observance made in March of 2025, by @Raysolva, who was not part of the initial project, so it may lack details and may hold false conclusions.


## `.dat` files by Michael Grier

These two files were used to generate separate dictionaries in several formats, non-uniformly by several persons. 

For further details, for both `.dat` files, Greek and Hebrew, same header is saying this:

> Dictionaries of Hebrew and Greek Words taken from `Strong's Exhaustive Concordance`, made by James Strong, S.T.D., LL.D. 1890
>
> E-text produced by Michael Grier <http://www.bigmweb.com/home/>
> 
> Corrected editions by:
>  - Ulrik Sandborg-Petersen <http://www.hum.aau.dk/~ulrikp/>
>  - Weston Ruter <http://weston.ruter.net/>
>  - Open Scriptures contributors <http://openscriptures.org/>


And the same message in them:

> ASCII e-text version:
> ---------------------
> 
> The files for this e-text were produced by Michael Grier, mgrier@pdnt.com, in 1996, and download from  http://members.tripod.com/~SoftIdeas, in February 1998. The files have been setup for importing into the Online Bible for DOS. But to make these files into generic text files, all that is needed is to replace the terms "GREEK" and "HEBREW" with "Greek" and "Hebrew" or the names of the appropriate files. 
> 
> The e-text has been changed from the printed version in three ways.
> 
> 1) A five digit Strong's word number with leading zeros has been placed before
>    each entry. 
> 2) Where Strong provides the number of another word for etymology,
>    a line with "see GREEK for" or "see HEBREW for" and the number, has been
>    added after Strong's entry for the word. (This is for use after
>    importing into the DOS version of Online Bible, but also provides a good
>    way to programmatically add links.)
> 3) The abbreviations used by Strong in the
>    Greek dictionary, (not Hebrew) have been replaced by the abbreviated words.
> 
> Michael Grier did a check of the e-text against a printed Strong's dictionary.
> The work seems clean but more proofreading is needed to certify it clean from
> errors.
> 
> Corrected edition:
> ------------------
> 
> The initial edition of this e-text requested errors to be reported to Bible Foundation. However, "Bible Foundation had to quit maintaining the e-text files but they live on and many people around the world have been greatly blessed." http://www.bf.org/bfetexts.htm
> 
> Ulrik Sandborg-Petersen <http://www.hum.aau.dk/~ulrikp/> and Weston Ruter <http://weston.ruter.net/> noticed several typos and errors in the text. Ulrik revised the Greek text and released another edition in XML including Unicode Greek, BETA code, and transliterations. Weston revised the e-texts as part of an effort to make a new unified XML document consisting of both the Greek and Hebrew entries. More information is available at http://openscriptures.org/
> 
> The initial Greek and Hebrew e-texts used for this corrected edition was downloaded from the SWORD project in December 2008:
>  - http://www.crosswire.org/sword/modules/ModInfo.jsp?modName=StrongsGreek
>  - http://www.crosswire.org/sword/modules/ModInfo.jsp?modName=StrongsHebrew
> Both of these modules were versioned at 1.2 and dated 2002-01-01. The incorporated revised Greek text by Ulrik Sandborg-Petersen was versioned at 1.4 and dated 2007-09-14 and was downloaded from the MorphGNT project:
>  - http://files.morphgnt.org/strongs-dictionary/StrongsGreekDictionaryXML_1.4.zip


## `.dic` files by Darrell H. Smith

These files is an addon made by Darrel Smith specifically to fulfill the need of original word spellings in UTF-8 signs of Hebrew and Greek languages, which are not present in `.dat` files. 
They were used exclusively to generate unified `.xhtml` dictionary of Greek and Hebrew, and are standalone amongst other files. 

The source of Hebrew `.dic` spellings is unknown; of Greek is probably an `.xml` file made by Ulrik Sandborg-Petersen. 


## (Hebrew+Greek) `.xhtml` unified dictionary by Darrell H. Smith

This is a separate work among other in this project. It is made based on `.dat` files, `.dic` files, and `strongsgreek.xml` file from `StrongsGreekDictionaryXML_1.4.zip`. 
Though it is not clear how exactly the last one was used, supposedly - spellings in signs of Greek language were taken from it into Greek `.dic` file. 

There is a header in it:

> Unified Strong's Dictionaries of Greek and Hebrew in XML
> Copyright (c) 2008, Open Scriptures <http://openscriptures.org/>.
> Freely released under GPL 3.0 license <http://www.gnu.org/licenses/gpl.html>
> This work is a derivative of the following:
>  - http://open-scriptures.googlecode.com/svn/trunk/sources/strongs-dictionaries/strongsgreek.dat
>  - http://open-scriptures.googlecode.com/svn/trunk/sources/strongs-dictionaries/strongshebrew.dat
>  - http://files.morphgnt.org/strongs-dictionary/StrongsGreekDictionaryXML_1.4.zip
> 
> 2009-05-20 Enhanced to include unicode spellings: Darrell H. Smith
> There are approx. 100 entries with no spelling fields (indicated by the token NONE);
> these are Hebrew words and a few Greek references to these Hebrew words; 
> this will be corrected

Tokens `NONE` had came from Hebrew `.dic` file into `.xhtml`, and where they are, there spellings are still missing; but all transliterations are present in `.xhtml` file, while being `NONE` in `.dic` file. 


## (Hebrew) `.xml` and `.js` dictionary by David Troidl 

It's not clear who made the last content correction to original `hebrewstrongs.dat` file, but XML was created from it by David Troidl (#75ea195), who then applied a lot of manual corrections to it, without modifying the original `.dat`.
Later, JS dict was added by David T. (#2f81622), based on his corrected XML. 

So, Hebrew `.dat` is the oldest, Hebrew `.xml` is very corrected, `.js` seems to be updated to be consistent with the latest Hebrew `.xml`, i.e. `StrongHebrewG.xml`.

It's not clear also, where Hebrew spellings came from into `.xml` dict, because `.dat` does not hold them. The `.dic` was not used as a source, manual check has shown that earliest Hebrew spellings in `.xml` and in `.dic` have differences. 

There is also a message in `StrongHebrewG.xml`, where PD supposedly means Public Domain, that gives a clue on that:

> <contributor role="edt">David Troidl</contributor>
> 
> <contributor role="edt">David Instone-Brewer</contributor>
> 
> <description>The data came from several PD sources which were full of errors. I cleaned them by comparing them to each other and (where necessary) looking at the original.</description>


## (Greek) `.xml` and `.js` dictionary by Ulrik Sandborg-Petersen

Greek dict in XML was made by Ulrik Petersen (lastly updated in 2007) out of `strongsgreek.dat` file. Petersen's work is stored in the folder `StrongsGreekDictionaryXML_1.4`, alongside with original `.dat` dictionary. 

Later, `strongsgreek.dat` had got correction by OpenScriptures, in particular by David Troidl, who then made a JS dict out of it. Corrected version is stored in the folder `greek/`, alongside with `.js` dictionary. 


# copyrights

### `.dat` files

> Copyright info:
> ---------------
> 
> Strong's Dictionaries of Hebrew and Greek Words were published in 1890
> and so are in the public domain. The original e-text was produced by Michael Grier
> which is also in the public domain. The revisions by Ulrik Sandborg-Petersen
> retained the public domain status. This corrected edition is released under the
> GPL 3.0 License:
>
> Copyright (c) 2008, OpenScriptures.org
>
> Permission is hereby granted, free of charge, to any person obtaining a copy
> of this software and associated documentation files (the "Software"), to deal
> in the Software without restriction, including without limitation the rights
> to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
> copies of the Software, and to permit persons to whom the Software is
> furnished to do so, subject to the following conditions:
> 
> The above copyright notice and this permission notice shall be included in
> all copies or substantial portions of the Software.
> 
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
> FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
> AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
> LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
> OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
> THE SOFTWARE.


### `.xhtml` file

> Unified Strong's Dictionaries of Greek and Hebrew in XML
> 
> Copyright (c) 2008, Open Scriptures <http://openscriptures.org/>.
> 
> Freely released under GPL 3.0 license <http://www.gnu.org/licenses/gpl.html>

### `.xml` files

Hebrew:
> Public Domain

Greek:
> Public Domain


### `.js` files

Hebrew:
> Copyright 2010, Open Scriptures. CC-BY-SA. Derived from XML.

Greek:
> Copyright 2009, Open Scriptures. CC-BY-SA. Derived from XML.

