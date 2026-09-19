---
title: "Aspose::Words::Layout::LayoutEntityType enum"
linktitle: "LayoutEntityType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::LayoutEntityType enum. Tipi delle entità di layout in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enum


Tipi delle entità di layout.

```cpp
enum class LayoutEntityType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | n/a | Valore predefinito. |
| Page | n/a | Rappresenta una pagina di un documento. La pagina può contenere entità figlio [Column](./), [HeaderFooter](./) e [Comment](./). |
| Column | n/a | Rappresenta una colonna di testo su una pagina. La colonna può avere le stesse entità figlio di [Cell](./), più le entità [Footnote](./), [Endnote](./) e [NoteSeparator](./). |
| Row | n/a | Rappresenta una riga di tabella. La riga può avere [Cell](./) come entità figlio. |
| Cell | n/a | Rappresenta una cella di tabella. La cella può avere entità figlio [Line](./) e [Row](./). |
| Line | n/a | Rappresenta una linea di caratteri di testo e oggetti in linea. La linea può avere entità figlio [Span](./). |
| Span | n/a | Rappresenta uno o più caratteri in una riga. Include caratteri speciali come marcatori di inizio/fine campo, segnalibri e commenti. Span non può avere entità figlie. |
| Footnote | n/a | Rappresenta un segnaposto per il contenuto della nota a piè di pagina. Footnote può avere entità figlie di [Note](./). |
| Endnote | n/a | Rappresenta un segnaposto per il contenuto della nota di chiusura. Endnote può avere entità figlie di [Note](./). |
| Note | n/a | Rappresenta un segnaposto per il contenuto della nota. Note può avere entità figlie di [Line](./) e [Row](./). |
| HeaderFooter | n/a | Rappresenta un segnaposto per il contenuto di intestazione/piè di pagina su una pagina. [HeaderFooter](../../aspose.words/headerfooter/) può avere entità figlie di [Line](./) e [Row](./). |
| TextBox | n/a | Rappresenta l'area di testo all'interno di una forma. Textbox può avere entità figlie di [Line](./) e [Row](./). |
| Comment | n/a | Rappresenta un segnaposto per il contenuto del commento. [Comment](../../aspose.words/comment/) può avere entità figlie di [Line](./) e [Row](./). |
| NoteSeparator | n/a | Rappresenta il separatore di nota a piè di pagina/nota di chiusura. NoteSeparator può avere entità figlie di [Line](./) e [Row](./). |

## Vedi anche

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
