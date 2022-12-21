# From Catch 26 to catch 37 and grouping back to best possible reports

Input: 26 problems to reproduce with one-liner reports
Output: 26 problems reproduced once and 11 more added
Cleaned output: N problems

INPUT: 
  * [ ] Css validator gives errors
  * [ ] Special character as start of line forces an extra line change in grey display box
  * [ ] Firefox text field does not clear with ctrl+R
  * [ ] html validator identifies 3 errors
  * [ ] You're / we're / They're contractions not recognised as violations of e-prime
  * [ ] Two words separated by line feed are counted as one
  * [ ] Human being is noun but recognised as violation
  * [ ] Space is considered only separator for words and special characters are counted as words
* [ ] Long text moves button outside user's access as vertical scroll is disabled
* [ ] id naming is inconsistent, some are camel case, others not
* [ ] Long texts without spaces go outside the grey area reserved for displaying the texts
* [ ] Red/blue on grey has bad contrast
* [ ] Zoom or resize of browser renders page unusable due to missing scroll bars
* [ ] Contractions for word count (I'm) count as two words as per general searchable rules of how word counting works
* [ ] The possible violation's category takes possessives and leaves for human assessment and would probably be expected to be something to create programmatic rules on
* [ ] Possible violations does not handle typesetter's apostrophe, only typewriter's apostrophe in calculation
* [ ] Two part words (like people's last names) in possessive form are not recognised as possible violations
* [ ] Images missing alt text necessary for accessibility
* [ ] Accessibility warnings on contrast
* [ ] Mobile use not supported, styles very non-responsive
* [ ] UI instructions for user are unclear
* [ ] if word is in single quotes, it is not properly recognised as e-prime. 
* [ ] text box location in UI is not where user would expect it to be as per the logic of how web pages are usually operating
* [ ] Site is missing favicon and security.txt - both common conventions for web applications
* [ ] Resizing the input text field can move it outside view so that it cannot be resized back
* [ ] Choosing which links are to overload this app and which open new browser window are inconsistent

ADDED:
  * word + space + enter creates extra vertical space in grey area
  * 'is are' both are not recognised
  * zoom with and horizontal bar has issues, seen on edge and chrome, on win and Mac with touchpad
  * wave accessibility tool does a forced refresh on close (tool)
  * On Chrome when settings panel open, scroll does not work. It works on Firefox. (tool)
  * Enter in end of line moves last word to different line on grey box
  * Firefox does not come back from mobile use simulation without forced refresh with this site
  * Image of license isn't readable: accessibility issue
  * Possible issue with scandinavian letters (ä, ö, å) and false violations (e.g. "isä")
  * License needs to be a text file exactly as it is given by legal
  * Mix of fonts, less would be cleaner

### Cleaned output

To be added.


## Bug Reports

### Missing vertical scroll bar makes button inaccessible with long input text

To repro: 
1. Open https://maaret.com/app (the not fixed deployment)
2. Copy e.g. the prime wikipedia page contents to the input field
3. Click 'Check for eprime'

Note: Unable to scroll vertically. 'Check for eprime' button not accessible to press for new text.

Tested only on Mac / Chrome + Firefox - no zoom applied. 
