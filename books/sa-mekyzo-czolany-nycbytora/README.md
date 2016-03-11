Sa mekyzo czolany nycbytora
===========================

A sample non-technical book (memoirs) with footnotes and index entries.

Tweaks
------

Several helpers are used to trigger specific treatment during the processing, 
but only if customized ConTeXt stylesheet is used.

|    Processing Instruction   |                 Purpose                  |  Default n |
|-----------------------------|------------------------------------------|:----------:|
| <?linebreak?>               | hard line break                          |     --     |
| <?linebreak?>               | hard line break                          |     --     |
| <?divider?>                 | narrow horizontal line                   |     --     |
| <?v-spacer lines="n"?>      | vertical spacer                          |      1     |
| <?hanging-indent size="n"?> | negative line indent                     |    0.7mm¹  |
| <?alignment tolerance="n"?> | alignment tolerance of the current block | verystrict²|

¹ Used to shift lines beginning with characters disturbing the optical edge (e.g. »)
² Blocks are aligned using the `verystrict` tolerance, which can lead to lines exceeding
  the text area. Such blocks can be tweaked by manual inserting PIs with the less strict 
  tolerance.

|      Custom Role Values     |                        Purpose                            |
|-----------------------------|-----------------------------------------------------------|
| para@role="verse"           | italicized text in the narrower block for verses          |
| indexterm@role="swap-space" | actually just remark for cases when the space before      |
|                             | indexterm was used for separating the element and         |
|                             | the adjacent text. When indexterm precedes optically      |
|                             | insignificant character, both parts have to be separated  |
|                             | by space otherwise that character is not 'hanged' outside |
|                             | the text area when hanging punctuation is enabled.¹       |

¹ Please compare
  ```
  word <indexterm type="subject"><primary sortas="term">»term«</primary></indexterm>»term«
  word<indexterm type="subject" role="swap-space"><primary sortas="term">»term«</primary></indexterm> »term«
  ```
