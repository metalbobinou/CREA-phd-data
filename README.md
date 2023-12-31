# CREA-phd-data
Data generated for the CREA method evaluation during my PhD.

Multiple scenarios are included (with the original documents) and a very small survey.

Structure of this README.md :
- Data: description of the documents and how they were organized
- Scenarios: description of the scenarios and which documents are used


The original CREA method prototype developped for my PhD is available here : [CREA-PhD](https://github.com/metalbobinou/CREA-phd)

The thesis manuscript (in french) can be found here : [PhD Thesis](https://theses.hal.science/tel-03774087v1) and [LaTeX sources](https://github.com/metalbobinou/CREA-phd-thesis)

The current state of the CREA method is available in another Git repository : [CREA](https://github.com/metalbobinou/CREA)


# Data

### Input Materials

- **C1 - C9** are courses on PHP, these are the main courses used for building the CREA method
- **C11 - C19** are courses on PHP, but these were added later in order to check how reliable the CREA method is when we double the number of inputs

- **CJA** is a Java course, it is used to test how the visualisation excludes an off topic document. Java has been chosen as it's still a development language slightly linked with the web, but absolutely not with PHP.

- *__C10__ is my own course materials. Therefore, I didn't included it within the regular scenarios. I still kept it in order to evaluate it later. (Two matrices included it : PHP+C10 and PHP+Java+C10)*


| Slide format      | Text format   |
|-------------------|---------------|
| C1 C2 C4 C7 C8 C9 | C3 C5 C6  CJA |
|C12 C13 C14 C16 C18|C11 C15 C17 C19|

|      |C1|C2|C3|C4|C5|C6|C7|C8|C9|CJA|
|------|--|--|--|--|--|--|--|--|--|---|
|Slides| x| x|  | x|  |  | x| x| x|   |
| Text |  |  | x|  | x| x|  |  |  | x |

|      |C11|C12|C13|C14|C15|C16|C17|C18|C19|
|------|---|---|---|---|---|---|---|---|---|
|Slides|   | x | x | x |   | x |   | x |   |
| Text | x |   |   |   | x |   | x |   | x |


### Matrices (6.1 Input Matrix)

- **PHP-automatic** is a matrix with the 9 PHP courses, it is the basic case [C1, C2, C3, C4, C5, C6, C7, C8, C9]
- **PHP+Java-automatic** is a matrix with the 9 PHP courses + a Java course (in full text format), in order to test how well the method excludes off topic documents [C1-C9, CJA]
- **PHP-automatic-18** is a matrix with 18 courses, in order to check how well the method supports twice the number of courses [C1-C9, C11-C19]

- **Full-Slides** is a matrix with only courses in slides format (11 courses) from the 18 [C1, C2, C4, C7, C8, C9, C12, C13, C14, C16, C18]
- __Full-Text-*__ are matrices based only on courses made with texts (no slide) from the 18 [C3, C5, C6, C11, C15, C17, C19]
- __Full-Text-C+noP-*__ are matrices with text only, but in __C6__ : *with* the "hors programme" (extra-curricular) part of the course (C), but *without* the students projects (noP)
- __Full-Text-noC+noP-*__ are matrices with text only, but in __C6__ : *without* the "hors programme" (extra-curricular) part of the course (noC), and *without* the students projects (noP)

- *__PHP-automatic+C10__ is a matrix with the 9 PHP course + my own course (C10) that I built (I didn't really tested this one)*

Various combinations can be found : Full-Text-noC-noP-PHP+Java, PHP+Java+C10, ...


# Scenarios

5 scenarios were designed in order to test the CREA method and some qualities :

- Scenario 1 *(reference case)*: the main scenario based on 9 PHP courses in french (6 in slides format, 3 in text format). The objective is to test if the method is able to work in one simple case. The visualisation and the clusters are produced.

- Scenario 2 *(noise resistance)*: a Java course in french (text format) is added to the reference case. The objective is to evaluate the resistance to the noise by checking how the Java course will be excluded on the visualisation. Only the visualisation is produced.

- Scenario 3 *(reliability)*: 9 additional courses in french are added to the reference case (5 in slides format, 4 in text format). The objective is to evaluate the reliability by checking if the results are still relevant when doubling the inputs. The visualisation and the clusters are produced.

- Scenario 4 *(correction)*: only text format courses are used, including the Java one (7 + 1 courses). The course C6 is corrected by deleting useless parts multiple times (first by deleting the reports of students' projects from the document, then by deleting extra-curriculum chapters). The objective is to test if the method is able to show if a document is more relevant when corrected. Only the visualisation is produced, but 6 times (only the PHP courses, only the PHP courses while deleting students' projects in C6, only the PHP courses while deleting students' projects and extra-curriculum in C6, the same previous cases while introducing the Java course).

- Scenario 5 *(another theme)*: 13 documents of various natures in english talking about Statecharts are used (5 research articles [A], and 8 presentations, web pages, and courses [C]). The objectives are first to check if the method, based on BabelFy and BabelNet, is able to manage english instead of french, and second to check if a less known topic than PHP (like Statecharts) is still managed by the CREA method. The visualisation and the clusters are produced.
