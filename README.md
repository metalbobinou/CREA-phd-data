# CREA-phd-data
Data generated for the CREA method evaluation during my PhD.

Multiple scenarios are included (with the original documents) and a very small survey.


The original CREA method prototype developped for my PhD is available here : [CREA-PhD](https://github.com/metalbobinou/CREA-phd)

The thesis manuscript (in french) can be found here : [PhD Thesis](https://theses.hal.science/tel-03774087v1)

The current state of the CREA method is available in another Git repository : [CREA](https://github.com/metalbobinou/CREA)

# Scenarios

# Data

## Input Materials

- **C10** is my own course materials. Therefore, I didn't included it within the regular scenarios. I still kept it in order to evaluate it later. (Two matrices included it : PHP+C10 and PHP+Java+C10)

- **C1 - C9** are courses on PHP, these are the main courses used for building the CREA method
- **C11 - C19** are courses on PHP, but these were added later in order to check of robust the CREA method is when we double the number of inputs
- **CJA** is a Java course
 
- C1, C2, C4, C7, C8, C9 are in *slides* format
- C3, C5, C6, and CJA  are in *text* format
 
- C12, C13, C14, C16, C19 are in *slides* format
- C11, C15, C17, C19 are in *text* format


## Matrices (6.1 Input Matrix)

- **PHP-automatic** is a matrix with the 9 PHP courses, it is the basic case [C1, C2, C3, C4, C5, C6, C7, C8, C9]
- **PHP+Java-automatic** is a matrix with the 9 PHP courses + a Java course (in full text format), in order to test how well the method excludes off topic documents
- **PHP-automatic-18** is a matrix with 18 courses, in order to check how well the method supports twice the number of courses [ C1-C9, C11-C19]
- **Full-Slides** is a matrix with only courses in slides format (11 courses) from the 18 [C1, C2, C4, C7, C8, C9, C12, C13, C14, C16, C18]
- __Full-Text-*__ are matrices based only on courses made with texts (no slide) from the 18 [C3, C5, C6, C11, C15, C17, C19]
- __Full-Text-C+noP-*__ are matrices with the "hors programme" (extra-curricular) part of the course (C), but without the students projects (noP)
- __Full-Text-noC+noP-*__ are matrices without the "hors programme" (extra-curricular) part of the course (noC), and without the students projects (noP)
- **PHP-automatic+C10** is a matrix with the 9 PHP course + my own course (C10) that I built (I didn't really tested this one)

Various combinations can be found : Full-Text-noC-noP-PHP+Java, PHP+Java+C10, ...

