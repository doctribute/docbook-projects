Sa mekyzo czolany nycbytora
===========================

A sample non-technical book (memoirs) with footnotes and index entries.

Tweaks
------

Several helpers are used to trigger specific treatment during the processing, 
but only if customized ConTeXt stylesheet is used.

|    Processing Instruction   |                 Purpose                  |  Default n |
|-----------------------------|------------------------------------------|:----------:|
| <?divider?>                 | narrow horizontal line                   |     --     |
| <?v-spacer lines="n"?>      | vertical spacer                          |      1     |
| <?alignment tolerance="n"?> | alignment tolerance of the current block | verystrict¹|

¹ Blocks are aligned using the `verystrict` tolerance, which can lead to lines exceeding
  the text area. Such blocks can be tweaked by manual inserting PIs with the less strict 
  tolerance.

|      Custom Role Values     |                    Purpose                     |
|-----------------------------|------------------------------------------------|
| simplelist@role="verse"     | Verses in the narrower block and italic style. |
