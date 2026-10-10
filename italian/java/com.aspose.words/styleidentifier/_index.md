---
title: "StyleIdentifier"
linktitle: "StyleIdentifier"
second_title: "Aspose.Words per Java"
description: "Identificatore di stile indipendente dalla locale in Java."
type: docs
weight: 643
url: /it/java/com.aspose.words/styleidentifier/
---

**Inheritance:**
java.lang.Object
```
public class StyleIdentifier
```

Identificatore di stile indipendente dalla locale.

 **Remarks:** 

I nomi degli stili predefiniti in MS Word sono localizzati per diverse lingue. Utilizzando un identificatore di stile è possibile trovare lo stile corretto indipendentemente dalla lingua del documento.

Tutti gli stili definiti dall'utente sono assegnati al valore [USER](../../com.aspose.words/styleidentifier/#USER).

 **Examples:** 

Mostra come modificare lo stile del testo esistente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of referencing styles.
 // 1 -  Using the style name:
 builder.getFont().setStyleName("Emphasis");
 builder.writeln("Text originally in \"Emphasis\" style");

 // 2 -  Using a built-in style identifier:
 builder.getFont().setStyleIdentifier(StyleIdentifier.INTENSE_EMPHASIS);
 builder.writeln("Text originally in \"Intense Emphasis\" style");

 // Convert all uses of one style to another,
 // using the above methods to reference old and new styles.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     if (run.getFont().getStyleName().equals("Emphasis"))
         run.getFont().setStyleName("Strong");

     if (((run.getFont().getStyleIdentifier()) == (StyleIdentifier.INTENSE_EMPHASIS)))
         run.getFont().setStyleIdentifier(StyleIdentifier.STRONG);
 }

 doc.save(getArtifactsDir() + "Font.ChangeStyle.docx");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [BALLOON_TEXT](#BALLOON-TEXT) |  |
| [BIBLIOGRAPHY](#BIBLIOGRAPHY) |  |
| [BLOCK_TEXT](#BLOCK-TEXT) |  |
| [BODY_TEXT](#BODY-TEXT) | Lo stile Testo del corpo. |
| [BODY_TEXT_1_I](#BODY-TEXT-1-I) |  |
| [BODY_TEXT_1_I_2](#BODY-TEXT-1-I-2) |  |
| [BODY_TEXT_2](#BODY-TEXT-2) |  |
| [BODY_TEXT_3](#BODY-TEXT-3) |  |
| [BODY_TEXT_IND](#BODY-TEXT-IND) |  |
| [BODY_TEXT_IND_2](#BODY-TEXT-IND-2) |  |
| [BODY_TEXT_IND_3](#BODY-TEXT-IND-3) |  |
| [BOOK_TITLE](#BOOK-TITLE) |  |
| [CAPTION](#CAPTION) |  |
| [CLOSING](#CLOSING) |  |
| [COLORFUL_GRID](#COLORFUL-GRID) |  |
| [COLORFUL_GRID_ACCENT_1](#COLORFUL-GRID-ACCENT-1) |  |
| [COLORFUL_GRID_ACCENT_2](#COLORFUL-GRID-ACCENT-2) |  |
| [COLORFUL_GRID_ACCENT_3](#COLORFUL-GRID-ACCENT-3) |  |
| [COLORFUL_GRID_ACCENT_4](#COLORFUL-GRID-ACCENT-4) |  |
| [COLORFUL_GRID_ACCENT_5](#COLORFUL-GRID-ACCENT-5) |  |
| [COLORFUL_GRID_ACCENT_6](#COLORFUL-GRID-ACCENT-6) |  |
| [COLORFUL_LIST](#COLORFUL-LIST) |  |
| [COLORFUL_LIST_ACCENT_1](#COLORFUL-LIST-ACCENT-1) |  |
| [COLORFUL_LIST_ACCENT_2](#COLORFUL-LIST-ACCENT-2) |  |
| [COLORFUL_LIST_ACCENT_3](#COLORFUL-LIST-ACCENT-3) |  |
| [COLORFUL_LIST_ACCENT_4](#COLORFUL-LIST-ACCENT-4) |  |
| [COLORFUL_LIST_ACCENT_5](#COLORFUL-LIST-ACCENT-5) |  |
| [COLORFUL_LIST_ACCENT_6](#COLORFUL-LIST-ACCENT-6) |  |
| [COLORFUL_SHADING](#COLORFUL-SHADING) |  |
| [COLORFUL_SHADING_ACCENT_1](#COLORFUL-SHADING-ACCENT-1) |  |
| [COLORFUL_SHADING_ACCENT_2](#COLORFUL-SHADING-ACCENT-2) |  |
| [COLORFUL_SHADING_ACCENT_3](#COLORFUL-SHADING-ACCENT-3) |  |
| [COLORFUL_SHADING_ACCENT_4](#COLORFUL-SHADING-ACCENT-4) |  |
| [COLORFUL_SHADING_ACCENT_5](#COLORFUL-SHADING-ACCENT-5) |  |
| [COLORFUL_SHADING_ACCENT_6](#COLORFUL-SHADING-ACCENT-6) |  |
| [COMMENT_REFERENCE](#COMMENT-REFERENCE) | Lo stile Riferimento dell'annotazione (commento). |
| [COMMENT_SUBJECT](#COMMENT-SUBJECT) |  |
| [COMMENT_TEXT](#COMMENT-TEXT) | Lo stile Testo dell'annotazione (commento). |
| [DARK_LIST](#DARK-LIST) |  |
| [DARK_LIST_ACCENT_1](#DARK-LIST-ACCENT-1) |  |
| [DARK_LIST_ACCENT_2](#DARK-LIST-ACCENT-2) |  |
| [DARK_LIST_ACCENT_3](#DARK-LIST-ACCENT-3) |  |
| [DARK_LIST_ACCENT_4](#DARK-LIST-ACCENT-4) |  |
| [DARK_LIST_ACCENT_5](#DARK-LIST-ACCENT-5) |  |
| [DARK_LIST_ACCENT_6](#DARK-LIST-ACCENT-6) |  |
| [DATE](#DATE) |  |
| [DEFAULT_PARAGRAPH_FONT](#DEFAULT-PARAGRAPH-FONT) | Lo stile Font di paragrafo predefinito. |
| [DOCUMENT_MAP](#DOCUMENT-MAP) |  |
| [EMAIL_SIGNATURE](#EMAIL-SIGNATURE) |  |
| [EMPHASIS](#EMPHASIS) |  |
| [ENDNOTE_REFERENCE](#ENDNOTE-REFERENCE) | Lo stile Riferimento della nota finale. |
| [ENDNOTE_TEXT](#ENDNOTE-TEXT) | Lo stile Testo della nota finale. |
| [ENVELOPE_ADDRESS](#ENVELOPE-ADDRESS) | Lo stile Indirizzo della busta. |
| [ENVELOPE_RETURN](#ENVELOPE-RETURN) | Lo stile Ritorno della busta. |
| [FOLLOWED_HYPERLINK](#FOLLOWED-HYPERLINK) |  |
| [FOOTER](#FOOTER) | Lo stile Piè di pagina. |
| [FOOTNOTE_REFERENCE](#FOOTNOTE-REFERENCE) | Lo stile Riferimento della nota a piè di pagina. |
| [FOOTNOTE_TEXT](#FOOTNOTE-TEXT) | Lo stile Testo della nota a piè di pagina. |
| [GRID_TABLE_1_LIGHT](#GRID-TABLE-1-LIGHT) | Tabella a griglia 1 chiara |
| [GRID_TABLE_1_LIGHT_ACCENT_1](#GRID-TABLE-1-LIGHT-ACCENT-1) | Tabella a griglia 1 chiara - Accento 1 |
| [GRID_TABLE_1_LIGHT_ACCENT_2](#GRID-TABLE-1-LIGHT-ACCENT-2) | Tabella a griglia 1 chiara - Accento 2 |
| [GRID_TABLE_1_LIGHT_ACCENT_3](#GRID-TABLE-1-LIGHT-ACCENT-3) | Tabella a griglia 1 chiara - Accento 3 |
| [GRID_TABLE_1_LIGHT_ACCENT_4](#GRID-TABLE-1-LIGHT-ACCENT-4) | Tabella a griglia 1 chiara - Accento 4 |
| [GRID_TABLE_1_LIGHT_ACCENT_5](#GRID-TABLE-1-LIGHT-ACCENT-5) | Tabella a griglia 1 chiara - Accento 5 |
| [GRID_TABLE_1_LIGHT_ACCENT_6](#GRID-TABLE-1-LIGHT-ACCENT-6) | Tabella a griglia 1 chiara - Accento 6 |
| [GRID_TABLE_2](#GRID-TABLE-2) | Tabella a griglia 2 |
| [GRID_TABLE_2_ACCENT_1](#GRID-TABLE-2-ACCENT-1) | Tabella a griglia 2 - Accento 1 |
| [GRID_TABLE_2_ACCENT_2](#GRID-TABLE-2-ACCENT-2) | Tabella a griglia 2 - Accento 2 |
| [GRID_TABLE_2_ACCENT_3](#GRID-TABLE-2-ACCENT-3) | Tabella a griglia 2 - Accento 3 |
| [GRID_TABLE_2_ACCENT_4](#GRID-TABLE-2-ACCENT-4) | Tabella a griglia 2 - Accento 4 |
| [GRID_TABLE_2_ACCENT_5](#GRID-TABLE-2-ACCENT-5) | Tabella a griglia 2 - Accento 5 |
| [GRID_TABLE_2_ACCENT_6](#GRID-TABLE-2-ACCENT-6) | Tabella a griglia 2 - Accento 6 |
| [GRID_TABLE_3](#GRID-TABLE-3) | Tabella a griglia 3 |
| [GRID_TABLE_3_ACCENT_1](#GRID-TABLE-3-ACCENT-1) | Tabella a griglia 3 - Accento 1 |
| [GRID_TABLE_3_ACCENT_2](#GRID-TABLE-3-ACCENT-2) | Tabella a griglia 3 - Accento 2 |
| [GRID_TABLE_3_ACCENT_3](#GRID-TABLE-3-ACCENT-3) | Tabella a griglia 3 - Accento 3 |
| [GRID_TABLE_3_ACCENT_4](#GRID-TABLE-3-ACCENT-4) | Tabella a griglia 3 - Accento 4 |
| [GRID_TABLE_3_ACCENT_5](#GRID-TABLE-3-ACCENT-5) | Tabella a griglia 3 - Accento 5 |
| [GRID_TABLE_3_ACCENT_6](#GRID-TABLE-3-ACCENT-6) | Tabella a griglia 3 - Accento 6 |
| [GRID_TABLE_4](#GRID-TABLE-4) | Tabella a griglia 4 |
| [GRID_TABLE_4_ACCENT_1](#GRID-TABLE-4-ACCENT-1) | Tabella a griglia 4 - Accento 1 |
| [GRID_TABLE_4_ACCENT_2](#GRID-TABLE-4-ACCENT-2) | Tabella a griglia 4 - Accento 2 |
| [GRID_TABLE_4_ACCENT_3](#GRID-TABLE-4-ACCENT-3) | Tabella a griglia 4 - Accento 3 |
| [GRID_TABLE_4_ACCENT_4](#GRID-TABLE-4-ACCENT-4) | Tabella a griglia 4 - Accento 4 |
| [GRID_TABLE_4_ACCENT_5](#GRID-TABLE-4-ACCENT-5) | Tabella a griglia 4 - Accento 5 |
| [GRID_TABLE_4_ACCENT_6](#GRID-TABLE-4-ACCENT-6) | Tabella a griglia 4 - Accento 6 |
| [GRID_TABLE_5_DARK](#GRID-TABLE-5-DARK) | Tabella a griglia 5 Scuro |
| [GRID_TABLE_5_DARK_ACCENT_1](#GRID-TABLE-5-DARK-ACCENT-1) | Tabella a griglia 5 Scuro - Accento 1 |
| [GRID_TABLE_5_DARK_ACCENT_2](#GRID-TABLE-5-DARK-ACCENT-2) | Tabella a griglia 5 Scuro - Accento 2 |
| [GRID_TABLE_5_DARK_ACCENT_3](#GRID-TABLE-5-DARK-ACCENT-3) | Tabella a griglia 5 Scuro - Accento 3 |
| [GRID_TABLE_5_DARK_ACCENT_4](#GRID-TABLE-5-DARK-ACCENT-4) | Tabella a griglia 5 Scuro - Accento 4 |
| [GRID_TABLE_5_DARK_ACCENT_5](#GRID-TABLE-5-DARK-ACCENT-5) | Tabella a griglia 5 Scuro - Accento 5 |
| [GRID_TABLE_5_DARK_ACCENT_6](#GRID-TABLE-5-DARK-ACCENT-6) | Tabella a griglia 5 Scuro - Accento 6 |
| [GRID_TABLE_6_COLORFUL](#GRID-TABLE-6-COLORFUL) | Tabella a griglia 6 Colorato |
| [GRID_TABLE_6_COLORFUL_ACCENT_1](#GRID-TABLE-6-COLORFUL-ACCENT-1) | Tabella a griglia 6 Colorata - Accento 1 |
| [GRID_TABLE_6_COLORFUL_ACCENT_2](#GRID-TABLE-6-COLORFUL-ACCENT-2) | Tabella a griglia 6 Colorata - Accento 2 |
| [GRID_TABLE_6_COLORFUL_ACCENT_3](#GRID-TABLE-6-COLORFUL-ACCENT-3) | Tabella a griglia 6 Colorata - Accento 3 |
| [GRID_TABLE_6_COLORFUL_ACCENT_4](#GRID-TABLE-6-COLORFUL-ACCENT-4) | Tabella a griglia 6 Colorata - Accento 4 |
| [GRID_TABLE_6_COLORFUL_ACCENT_5](#GRID-TABLE-6-COLORFUL-ACCENT-5) | Tabella a griglia 6 Colorata - Accento 5 |
| [GRID_TABLE_6_COLORFUL_ACCENT_6](#GRID-TABLE-6-COLORFUL-ACCENT-6) | Tabella a griglia 6 Colorata - Accento 6 |
| [GRID_TABLE_7_COLORFUL](#GRID-TABLE-7-COLORFUL) | Tabella a griglia 7 Colorata |
| [GRID_TABLE_7_COLORFUL_ACCENT_1](#GRID-TABLE-7-COLORFUL-ACCENT-1) | Tabella a griglia 7 Colorata - Accento 1 |
| [GRID_TABLE_7_COLORFUL_ACCENT_2](#GRID-TABLE-7-COLORFUL-ACCENT-2) | Tabella a griglia 7 Colorata - Accento 2 |
| [GRID_TABLE_7_COLORFUL_ACCENT_3](#GRID-TABLE-7-COLORFUL-ACCENT-3) | Tabella a griglia 7 Colorata - Accento 3 |
| [GRID_TABLE_7_COLORFUL_ACCENT_4](#GRID-TABLE-7-COLORFUL-ACCENT-4) | Tabella a griglia 7 Colorata - Accento 4 |
| [GRID_TABLE_7_COLORFUL_ACCENT_5](#GRID-TABLE-7-COLORFUL-ACCENT-5) | Tabella a griglia 7 Colorata - Accento 5 |
| [GRID_TABLE_7_COLORFUL_ACCENT_6](#GRID-TABLE-7-COLORFUL-ACCENT-6) | Tabella a griglia 7 Colorata - Accento 6 |
| [HASHTAG](#HASHTAG) | Lo stile Hashtag. |
| [HEADER](#HEADER) | Lo stile Header. |
| [HEADING_1](#HEADING-1) | Lo stile Titolo 1. |
| [HEADING_2](#HEADING-2) | Lo stile Titolo 2. |
| [HEADING_3](#HEADING-3) | Lo stile Titolo 3. |
| [HEADING_4](#HEADING-4) | Lo stile Titolo 4. |
| [HEADING_5](#HEADING-5) | Lo stile Titolo 5. |
| [HEADING_6](#HEADING-6) | Lo stile Titolo 6. |
| [HEADING_7](#HEADING-7) | Lo stile Titolo 7. |
| [HEADING_8](#HEADING-8) | Lo stile Titolo 8. |
| [HEADING_9](#HEADING-9) | Lo stile Titolo 9. |
| [HTML_ACRONYM](#HTML-ACRONYM) |  |
| [HTML_ADDRESS](#HTML-ADDRESS) |  |
| [HTML_BOTTOM_OF_FORM](#HTML-BOTTOM-OF-FORM) |  |
| [HTML_CITE](#HTML-CITE) |  |
| [HTML_CODE](#HTML-CODE) |  |
| [HTML_DEFINITION](#HTML-DEFINITION) |  |
| [HTML_KEYBOARD](#HTML-KEYBOARD) |  |
| [HTML_PREFORMATTED](#HTML-PREFORMATTED) |  |
| [HTML_SAMPLE](#HTML-SAMPLE) |  |
| [HTML_TOP_OF_FORM](#HTML-TOP-OF-FORM) |  |
| [HTML_TYPEWRITER](#HTML-TYPEWRITER) |  |
| [HTML_VARIABLE](#HTML-VARIABLE) |  |
| [HYPERLINK](#HYPERLINK) | Lo stile Hyperlink. |
| [INDEX_1](#INDEX-1) |  |
| [INDEX_2](#INDEX-2) |  |
| [INDEX_3](#INDEX-3) |  |
| [INDEX_4](#INDEX-4) |  |
| [INDEX_5](#INDEX-5) |  |
| [INDEX_6](#INDEX-6) |  |
| [INDEX_7](#INDEX-7) |  |
| [INDEX_8](#INDEX-8) |  |
| [INDEX_9](#INDEX-9) |  |
| [INDEX_HEADING](#INDEX-HEADING) | Lo stile intestazione indice. |
| [INTENSE_EMPHASIS](#INTENSE-EMPHASIS) |  |
| [INTENSE_QUOTE](#INTENSE-QUOTE) |  |
| [INTENSE_REFERENCE](#INTENSE-REFERENCE) |  |
| [LIGHT_GRID](#LIGHT-GRID) |  |
| [LIGHT_GRID_ACCENT_1](#LIGHT-GRID-ACCENT-1) |  |
| [LIGHT_GRID_ACCENT_2](#LIGHT-GRID-ACCENT-2) |  |
| [LIGHT_GRID_ACCENT_3](#LIGHT-GRID-ACCENT-3) |  |
| [LIGHT_GRID_ACCENT_4](#LIGHT-GRID-ACCENT-4) |  |
| [LIGHT_GRID_ACCENT_5](#LIGHT-GRID-ACCENT-5) |  |
| [LIGHT_GRID_ACCENT_6](#LIGHT-GRID-ACCENT-6) |  |
| [LIGHT_LIST](#LIGHT-LIST) |  |
| [LIGHT_LIST_ACCENT_1](#LIGHT-LIST-ACCENT-1) |  |
| [LIGHT_LIST_ACCENT_2](#LIGHT-LIST-ACCENT-2) |  |
| [LIGHT_LIST_ACCENT_3](#LIGHT-LIST-ACCENT-3) |  |
| [LIGHT_LIST_ACCENT_4](#LIGHT-LIST-ACCENT-4) |  |
| [LIGHT_LIST_ACCENT_5](#LIGHT-LIST-ACCENT-5) |  |
| [LIGHT_LIST_ACCENT_6](#LIGHT-LIST-ACCENT-6) |  |
| [LIGHT_SHADING](#LIGHT-SHADING) |  |
| [LIGHT_SHADING_ACCENT_1](#LIGHT-SHADING-ACCENT-1) |  |
| [LIGHT_SHADING_ACCENT_2](#LIGHT-SHADING-ACCENT-2) |  |
| [LIGHT_SHADING_ACCENT_3](#LIGHT-SHADING-ACCENT-3) |  |
| [LIGHT_SHADING_ACCENT_4](#LIGHT-SHADING-ACCENT-4) |  |
| [LIGHT_SHADING_ACCENT_5](#LIGHT-SHADING-ACCENT-5) |  |
| [LIGHT_SHADING_ACCENT_6](#LIGHT-SHADING-ACCENT-6) |  |
| [LINE_NUMBER](#LINE-NUMBER) | Lo stile numero di riga. |
| [LIST](#LIST) | Lo stile elenco. |
| [LIST_2](#LIST-2) |  |
| [LIST_3](#LIST-3) |  |
| [LIST_4](#LIST-4) |  |
| [LIST_5](#LIST-5) |  |
| [LIST_BULLET](#LIST-BULLET) | Lo stile elenco puntato. |
| [LIST_BULLET_2](#LIST-BULLET-2) |  |
| [LIST_BULLET_3](#LIST-BULLET-3) |  |
| [LIST_BULLET_4](#LIST-BULLET-4) |  |
| [LIST_BULLET_5](#LIST-BULLET-5) |  |
| [LIST_CONTINUE](#LIST-CONTINUE) |  |
| [LIST_CONTINUE_2](#LIST-CONTINUE-2) |  |
| [LIST_CONTINUE_3](#LIST-CONTINUE-3) |  |
| [LIST_CONTINUE_4](#LIST-CONTINUE-4) |  |
| [LIST_CONTINUE_5](#LIST-CONTINUE-5) |  |
| [LIST_NUMBER](#LIST-NUMBER) | Lo stile elenco numerato. |
| [LIST_NUMBER_2](#LIST-NUMBER-2) |  |
| [LIST_NUMBER_3](#LIST-NUMBER-3) |  |
| [LIST_NUMBER_4](#LIST-NUMBER-4) |  |
| [LIST_NUMBER_5](#LIST-NUMBER-5) |  |
| [LIST_PARAGRAPH](#LIST-PARAGRAPH) |  |
| [LIST_TABLE_1_LIGHT](#LIST-TABLE-1-LIGHT) | Lista Tabella 1 Chiara |
| [LIST_TABLE_1_LIGHT_ACCENT_1](#LIST-TABLE-1-LIGHT-ACCENT-1) | Lista Tabella 1 Chiara - Accento 1 |
| [LIST_TABLE_1_LIGHT_ACCENT_2](#LIST-TABLE-1-LIGHT-ACCENT-2) | Lista Tabella 1 Chiara - Accento 2 |
| [LIST_TABLE_1_LIGHT_ACCENT_3](#LIST-TABLE-1-LIGHT-ACCENT-3) | Lista Tabella 1 Chiara - Accento 3 |
| [LIST_TABLE_1_LIGHT_ACCENT_4](#LIST-TABLE-1-LIGHT-ACCENT-4) | Lista Tabella 1 Chiara - Accento 4 |
| [LIST_TABLE_1_LIGHT_ACCENT_5](#LIST-TABLE-1-LIGHT-ACCENT-5) | Lista Tabella 1 Chiara - Accento 5 |
| [LIST_TABLE_1_LIGHT_ACCENT_6](#LIST-TABLE-1-LIGHT-ACCENT-6) | Lista Tabella 1 Chiara - Accento 6 |
| [LIST_TABLE_2](#LIST-TABLE-2) | Lista Tabella 2 |
| [LIST_TABLE_2_ACCENT_1](#LIST-TABLE-2-ACCENT-1) | Lista Tabella 2 - Accento 1 |
| [LIST_TABLE_2_ACCENT_2](#LIST-TABLE-2-ACCENT-2) | Lista Tabella 2 - Accento 2 |
| [LIST_TABLE_2_ACCENT_3](#LIST-TABLE-2-ACCENT-3) | Lista Tabella 2 - Accento 3 |
| [LIST_TABLE_2_ACCENT_4](#LIST-TABLE-2-ACCENT-4) | Lista Tabella 2 - Accento 4 |
| [LIST_TABLE_2_ACCENT_5](#LIST-TABLE-2-ACCENT-5) | Lista Tabella 2 - Accento 5 |
| [LIST_TABLE_2_ACCENT_6](#LIST-TABLE-2-ACCENT-6) | Lista Tabella 2 - Accento 6 |
| [LIST_TABLE_3](#LIST-TABLE-3) | Lista Tabella 3 |
| [LIST_TABLE_3_ACCENT_1](#LIST-TABLE-3-ACCENT-1) | Lista Tabella 3 - Accento 1 |
| [LIST_TABLE_3_ACCENT_2](#LIST-TABLE-3-ACCENT-2) | Lista Tabella 3 - Accento 2 |
| [LIST_TABLE_3_ACCENT_3](#LIST-TABLE-3-ACCENT-3) | Lista Tabella 3 - Accento 3 |
| [LIST_TABLE_3_ACCENT_4](#LIST-TABLE-3-ACCENT-4) | Lista Tabella 3 - Accento 4 |
| [LIST_TABLE_3_ACCENT_5](#LIST-TABLE-3-ACCENT-5) | Lista Tabella 3 - Accento 5 |
| [LIST_TABLE_3_ACCENT_6](#LIST-TABLE-3-ACCENT-6) | Elenco Tabella 3 - Accento 6 |
| [LIST_TABLE_4](#LIST-TABLE-4) | Elenco Tabella 4 |
| [LIST_TABLE_4_ACCENT_1](#LIST-TABLE-4-ACCENT-1) | Elenco Tabella 4 - Accento 1 |
| [LIST_TABLE_4_ACCENT_2](#LIST-TABLE-4-ACCENT-2) | Elenco Tabella 4 - Accento 2 |
| [LIST_TABLE_4_ACCENT_3](#LIST-TABLE-4-ACCENT-3) | Elenco Tabella 4 - Accento 3 |
| [LIST_TABLE_4_ACCENT_4](#LIST-TABLE-4-ACCENT-4) | Elenco Tabella 4 - Accento 4 |
| [LIST_TABLE_4_ACCENT_5](#LIST-TABLE-4-ACCENT-5) | Elenco Tabella 4 - Accento 5 |
| [LIST_TABLE_4_ACCENT_6](#LIST-TABLE-4-ACCENT-6) | Elenco Tabella 4 - Accento 6 |
| [LIST_TABLE_5_DARK](#LIST-TABLE-5-DARK) | Elenco Tabella 5 Scuro |
| [LIST_TABLE_5_DARK_ACCENT_1](#LIST-TABLE-5-DARK-ACCENT-1) | Elenco Tabella 5 Scuro - Accento 1 |
| [LIST_TABLE_5_DARK_ACCENT_2](#LIST-TABLE-5-DARK-ACCENT-2) | Elenco Tabella 5 Scuro - Accento 2 |
| [LIST_TABLE_5_DARK_ACCENT_3](#LIST-TABLE-5-DARK-ACCENT-3) | Elenco Tabella 5 Scuro - Accento 3 |
| [LIST_TABLE_5_DARK_ACCENT_4](#LIST-TABLE-5-DARK-ACCENT-4) | Elenco Tabella 5 Scuro - Accento 4 |
| [LIST_TABLE_5_DARK_ACCENT_5](#LIST-TABLE-5-DARK-ACCENT-5) | Elenco Tabella 5 Scuro - Accento 5 |
| [LIST_TABLE_5_DARK_ACCENT_6](#LIST-TABLE-5-DARK-ACCENT-6) | Elenco Tabella 5 Scuro - Accento 6 |
| [LIST_TABLE_6_COLORFUL](#LIST-TABLE-6-COLORFUL) | Elenco Tabella 6 Colorato |
| [LIST_TABLE_6_COLORFUL_ACCENT_1](#LIST-TABLE-6-COLORFUL-ACCENT-1) | Elenco Tabella 6 Colorato - Accento 1 |
| [LIST_TABLE_6_COLORFUL_ACCENT_2](#LIST-TABLE-6-COLORFUL-ACCENT-2) | Elenco Tabella 6 Colorato - Accento 2 |
| [LIST_TABLE_6_COLORFUL_ACCENT_3](#LIST-TABLE-6-COLORFUL-ACCENT-3) | Elenco Tabella 6 Colorato - Accento 3 |
| [LIST_TABLE_6_COLORFUL_ACCENT_4](#LIST-TABLE-6-COLORFUL-ACCENT-4) | Elenco Tabella 6 Colorato - Accento 4 |
| [LIST_TABLE_6_COLORFUL_ACCENT_5](#LIST-TABLE-6-COLORFUL-ACCENT-5) | Elenco Tabella 6 Colorato - Accento 5 |
| [LIST_TABLE_6_COLORFUL_ACCENT_6](#LIST-TABLE-6-COLORFUL-ACCENT-6) | Elenco Tabella 6 Colorato - Accento 6 |
| [LIST_TABLE_7_COLORFUL](#LIST-TABLE-7-COLORFUL) | Elenco Tabella 7 Colorato |
| [LIST_TABLE_7_COLORFUL_ACCENT_1](#LIST-TABLE-7-COLORFUL-ACCENT-1) | Elenco Tabella 7 Colorato - Accento 1 |
| [LIST_TABLE_7_COLORFUL_ACCENT_2](#LIST-TABLE-7-COLORFUL-ACCENT-2) | Elenco Tabella 7 Colorato - Accento 2 |
| [LIST_TABLE_7_COLORFUL_ACCENT_3](#LIST-TABLE-7-COLORFUL-ACCENT-3) | Elenco Tabella 7 Colorato - Accento 3 |
| [LIST_TABLE_7_COLORFUL_ACCENT_4](#LIST-TABLE-7-COLORFUL-ACCENT-4) | Elenco Tabella 7 Colorato - Accento 4 |
| [LIST_TABLE_7_COLORFUL_ACCENT_5](#LIST-TABLE-7-COLORFUL-ACCENT-5) | Elenco Tabella 7 Colorato - Accento 5 |
| [LIST_TABLE_7_COLORFUL_ACCENT_6](#LIST-TABLE-7-COLORFUL-ACCENT-6) | Elenco Tabella 7 Colorato - Accento 6 |
| [MACRO](#MACRO) |  |
| [MEDIUM_GRID_1](#MEDIUM-GRID-1) |  |
| [MEDIUM_GRID_1_ACCENT_1](#MEDIUM-GRID-1-ACCENT-1) |  |
| [MEDIUM_GRID_1_ACCENT_2](#MEDIUM-GRID-1-ACCENT-2) |  |
| [MEDIUM_GRID_1_ACCENT_3](#MEDIUM-GRID-1-ACCENT-3) |  |
| [MEDIUM_GRID_1_ACCENT_4](#MEDIUM-GRID-1-ACCENT-4) |  |
| [MEDIUM_GRID_1_ACCENT_5](#MEDIUM-GRID-1-ACCENT-5) |  |
| [MEDIUM_GRID_1_ACCENT_6](#MEDIUM-GRID-1-ACCENT-6) |  |
| [MEDIUM_GRID_2](#MEDIUM-GRID-2) |  |
| [MEDIUM_GRID_2_ACCENT_1](#MEDIUM-GRID-2-ACCENT-1) |  |
| [MEDIUM_GRID_2_ACCENT_2](#MEDIUM-GRID-2-ACCENT-2) |  |
| [MEDIUM_GRID_2_ACCENT_3](#MEDIUM-GRID-2-ACCENT-3) |  |
| [MEDIUM_GRID_2_ACCENT_4](#MEDIUM-GRID-2-ACCENT-4) |  |
| [MEDIUM_GRID_2_ACCENT_5](#MEDIUM-GRID-2-ACCENT-5) |  |
| [MEDIUM_GRID_2_ACCENT_6](#MEDIUM-GRID-2-ACCENT-6) |  |
| [MEDIUM_GRID_3](#MEDIUM-GRID-3) |  |
| [MEDIUM_GRID_3_ACCENT_1](#MEDIUM-GRID-3-ACCENT-1) |  |
| [MEDIUM_GRID_3_ACCENT_2](#MEDIUM-GRID-3-ACCENT-2) |  |
| [MEDIUM_GRID_3_ACCENT_3](#MEDIUM-GRID-3-ACCENT-3) |  |
| [MEDIUM_GRID_3_ACCENT_4](#MEDIUM-GRID-3-ACCENT-4) |  |
| [MEDIUM_GRID_3_ACCENT_5](#MEDIUM-GRID-3-ACCENT-5) |  |
| [MEDIUM_GRID_3_ACCENT_6](#MEDIUM-GRID-3-ACCENT-6) |  |
| [MEDIUM_LIST_1](#MEDIUM-LIST-1) |  |
| [MEDIUM_LIST_1_ACCENT_1](#MEDIUM-LIST-1-ACCENT-1) |  |
| [MEDIUM_LIST_1_ACCENT_2](#MEDIUM-LIST-1-ACCENT-2) |  |
| [MEDIUM_LIST_1_ACCENT_3](#MEDIUM-LIST-1-ACCENT-3) |  |
| [MEDIUM_LIST_1_ACCENT_4](#MEDIUM-LIST-1-ACCENT-4) |  |
| [MEDIUM_LIST_1_ACCENT_5](#MEDIUM-LIST-1-ACCENT-5) |  |
| [MEDIUM_LIST_1_ACCENT_6](#MEDIUM-LIST-1-ACCENT-6) |  |
| [MEDIUM_LIST_2](#MEDIUM-LIST-2) |  |
| [MEDIUM_LIST_2_ACCENT_1](#MEDIUM-LIST-2-ACCENT-1) |  |
| [MEDIUM_LIST_2_ACCENT_2](#MEDIUM-LIST-2-ACCENT-2) |  |
| [MEDIUM_LIST_2_ACCENT_3](#MEDIUM-LIST-2-ACCENT-3) |  |
| [MEDIUM_LIST_2_ACCENT_4](#MEDIUM-LIST-2-ACCENT-4) |  |
| [MEDIUM_LIST_2_ACCENT_5](#MEDIUM-LIST-2-ACCENT-5) |  |
| [MEDIUM_LIST_2_ACCENT_6](#MEDIUM-LIST-2-ACCENT-6) |  |
| [MEDIUM_SHADING_1](#MEDIUM-SHADING-1) |  |
| [MEDIUM_SHADING_1_ACCENT_1](#MEDIUM-SHADING-1-ACCENT-1) |  |
| [MEDIUM_SHADING_1_ACCENT_2](#MEDIUM-SHADING-1-ACCENT-2) |  |
| [MEDIUM_SHADING_1_ACCENT_3](#MEDIUM-SHADING-1-ACCENT-3) |  |
| [MEDIUM_SHADING_1_ACCENT_4](#MEDIUM-SHADING-1-ACCENT-4) |  |
| [MEDIUM_SHADING_1_ACCENT_5](#MEDIUM-SHADING-1-ACCENT-5) |  |
| [MEDIUM_SHADING_1_ACCENT_6](#MEDIUM-SHADING-1-ACCENT-6) |  |
| [MEDIUM_SHADING_2](#MEDIUM-SHADING-2) |  |
| [MEDIUM_SHADING_2_ACCENT_1](#MEDIUM-SHADING-2-ACCENT-1) |  |
| [MEDIUM_SHADING_2_ACCENT_2](#MEDIUM-SHADING-2-ACCENT-2) |  |
| [MEDIUM_SHADING_2_ACCENT_3](#MEDIUM-SHADING-2-ACCENT-3) |  |
| [MEDIUM_SHADING_2_ACCENT_4](#MEDIUM-SHADING-2-ACCENT-4) |  |
| [MEDIUM_SHADING_2_ACCENT_5](#MEDIUM-SHADING-2-ACCENT-5) |  |
| [MEDIUM_SHADING_2_ACCENT_6](#MEDIUM-SHADING-2-ACCENT-6) |  |
| [MENTION](#MENTION) | Lo stile Mention. |
| [MESSAGE_HEADER](#MESSAGE-HEADER) |  |
| [NIL](#NIL) | Riservato per uso interno. |
| [NORMAL](#NORMAL) | Lo stile Normal. |
| [NORMAL_INDENT](#NORMAL-INDENT) | Lo stile Normal Indent. |
| [NORMAL_WEB](#NORMAL-WEB) |  |
| [NOTE_HEADING](#NOTE-HEADING) |  |
| [NO_LIST](#NO-LIST) |  |
| [NO_SPACING](#NO-SPACING) |  |
| [OUTLINE_LIST_1](#OUTLINE-LIST-1) | Lo stile 1 / a / i. |
| [OUTLINE_LIST_2](#OUTLINE-LIST-2) | Lo stile 1 / 1.1 / 1.1.1. |
| [OUTLINE_LIST_3](#OUTLINE-LIST-3) | Lo stile Article / Section. |
| [PAGE_NUMBER](#PAGE-NUMBER) | Lo stile Page Number. |
| [PLACEHOLDER_TEXT](#PLACEHOLDER-TEXT) |  |
| [PLAIN_TABLE_1](#PLAIN-TABLE-1) | Tabella Semplice 1 |
| [PLAIN_TABLE_2](#PLAIN-TABLE-2) | Tabella Semplice 2 |
| [PLAIN_TABLE_3](#PLAIN-TABLE-3) | Tabella Semplice 3 |
| [PLAIN_TABLE_4](#PLAIN-TABLE-4) | Tabella Semplice 4 |
| [PLAIN_TABLE_5](#PLAIN-TABLE-5) | Tabella Semplice 5 |
| [PLAIN_TEXT](#PLAIN-TEXT) |  |
| [QUOTE](#QUOTE) |  |
| [REVISION](#REVISION) |  |
| [SALUTATION](#SALUTATION) |  |
| [SIGNATURE](#SIGNATURE) |  |
| [SMART_HYPERLINK](#SMART-HYPERLINK) | Lo stile SmartHyperlink. |
| [SMART_LINK](#SMART-LINK) | Lo stile Smart Link. |
| [STRONG](#STRONG) |  |
| [SUBTITLE](#SUBTITLE) |  |
| [SUBTLE_EMPHASIS](#SUBTLE-EMPHASIS) |  |
| [SUBTLE_REFERENCE](#SUBTLE-REFERENCE) |  |
| [TABLE_3_D_EFFECTS_1](#TABLE-3-D-EFFECTS-1) |  |
| [TABLE_3_D_EFFECTS_2](#TABLE-3-D-EFFECTS-2) |  |
| [TABLE_3_D_EFFECTS_3](#TABLE-3-D-EFFECTS-3) |  |
| [TABLE_CLASSIC_1](#TABLE-CLASSIC-1) |  |
| [TABLE_CLASSIC_2](#TABLE-CLASSIC-2) |  |
| [TABLE_CLASSIC_3](#TABLE-CLASSIC-3) |  |
| [TABLE_CLASSIC_4](#TABLE-CLASSIC-4) |  |
| [TABLE_COLORFUL_1](#TABLE-COLORFUL-1) |  |
| [TABLE_COLORFUL_2](#TABLE-COLORFUL-2) |  |
| [TABLE_COLORFUL_3](#TABLE-COLORFUL-3) |  |
| [TABLE_COLUMNS_1](#TABLE-COLUMNS-1) |  |
| [TABLE_COLUMNS_2](#TABLE-COLUMNS-2) |  |
| [TABLE_COLUMNS_3](#TABLE-COLUMNS-3) |  |
| [TABLE_COLUMNS_4](#TABLE-COLUMNS-4) |  |
| [TABLE_COLUMNS_5](#TABLE-COLUMNS-5) |  |
| [TABLE_CONTEMPORARY](#TABLE-CONTEMPORARY) |  |
| [TABLE_ELEGANT](#TABLE-ELEGANT) |  |
| [TABLE_GRID](#TABLE-GRID) |  |
| [TABLE_GRID_1](#TABLE-GRID-1) |  |
| [TABLE_GRID_2](#TABLE-GRID-2) |  |
| [TABLE_GRID_3](#TABLE-GRID-3) |  |
| [TABLE_GRID_4](#TABLE-GRID-4) |  |
| [TABLE_GRID_5](#TABLE-GRID-5) |  |
| [TABLE_GRID_6](#TABLE-GRID-6) |  |
| [TABLE_GRID_7](#TABLE-GRID-7) |  |
| [TABLE_GRID_8](#TABLE-GRID-8) |  |
| [TABLE_GRID_LIGHT](#TABLE-GRID-LIGHT) | Tabella Griglia Leggera |
| [TABLE_LIST_1](#TABLE-LIST-1) |  |
| [TABLE_LIST_2](#TABLE-LIST-2) |  |
| [TABLE_LIST_3](#TABLE-LIST-3) |  |
| [TABLE_LIST_4](#TABLE-LIST-4) |  |
| [TABLE_LIST_5](#TABLE-LIST-5) |  |
| [TABLE_LIST_6](#TABLE-LIST-6) |  |
| [TABLE_LIST_7](#TABLE-LIST-7) |  |
| [TABLE_LIST_8](#TABLE-LIST-8) |  |
| [TABLE_NORMAL](#TABLE-NORMAL) |  |
| [TABLE_OF_AUTHORITIES](#TABLE-OF-AUTHORITIES) |  |
| [TABLE_OF_FIGURES](#TABLE-OF-FIGURES) | Lo stile Tabella delle Figure. |
| [TABLE_PROFESSIONAL](#TABLE-PROFESSIONAL) |  |
| [TABLE_SIMPLE_1](#TABLE-SIMPLE-1) |  |
| [TABLE_SIMPLE_2](#TABLE-SIMPLE-2) |  |
| [TABLE_SIMPLE_3](#TABLE-SIMPLE-3) |  |
| [TABLE_SUBTLE_1](#TABLE-SUBTLE-1) |  |
| [TABLE_SUBTLE_2](#TABLE-SUBTLE-2) |  |
| [TABLE_THEME](#TABLE-THEME) |  |
| [TABLE_WEB_1](#TABLE-WEB-1) |  |
| [TABLE_WEB_2](#TABLE-WEB-2) |  |
| [TABLE_WEB_3](#TABLE-WEB-3) |  |
| [TITLE](#TITLE) | Lo stile Title. |
| [TOA_HEADING](#TOA-HEADING) |  |
| [TOC_1](#TOC-1) |  |
| [TOC_2](#TOC-2) |  |
| [TOC_3](#TOC-3) |  |
| [TOC_4](#TOC-4) |  |
| [TOC_5](#TOC-5) |  |
| [TOC_6](#TOC-6) |  |
| [TOC_7](#TOC-7) |  |
| [TOC_8](#TOC-8) |  |
| [TOC_9](#TOC-9) |  |
| [TOC_HEADING](#TOC-HEADING) |  |
| [UNRESOLVED_MENTION](#UNRESOLVED-MENTION) | Lo stile UnresolvedMention. |
| [USER](#USER) | Uno stile definito dall'utente. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String styleIdentifierName)](#fromName-java.lang.String) |  |
| [getName(int styleIdentifier)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int styleIdentifier)](#toString-int) |  |
### BALLOON_TEXT {#BALLOON-TEXT}
```
public static int BALLOON_TEXT
```




### BIBLIOGRAPHY {#BIBLIOGRAPHY}
```
public static int BIBLIOGRAPHY
```




### BLOCK_TEXT {#BLOCK-TEXT}
```
public static int BLOCK_TEXT
```




### BODY_TEXT {#BODY-TEXT}
```
public static int BODY_TEXT
```


Lo stile Testo del corpo.

### BODY_TEXT_1_I {#BODY-TEXT-1-I}
```
public static int BODY_TEXT_1_I
```




### BODY_TEXT_1_I_2 {#BODY-TEXT-1-I-2}
```
public static int BODY_TEXT_1_I_2
```




### BODY_TEXT_2 {#BODY-TEXT-2}
```
public static int BODY_TEXT_2
```




### BODY_TEXT_3 {#BODY-TEXT-3}
```
public static int BODY_TEXT_3
```




### BODY_TEXT_IND {#BODY-TEXT-IND}
```
public static int BODY_TEXT_IND
```




### BODY_TEXT_IND_2 {#BODY-TEXT-IND-2}
```
public static int BODY_TEXT_IND_2
```




### BODY_TEXT_IND_3 {#BODY-TEXT-IND-3}
```
public static int BODY_TEXT_IND_3
```




### BOOK_TITLE {#BOOK-TITLE}
```
public static int BOOK_TITLE
```




### CAPTION {#CAPTION}
```
public static int CAPTION
```




### CLOSING {#CLOSING}
```
public static int CLOSING
```




### COLORFUL_GRID {#COLORFUL-GRID}
```
public static int COLORFUL_GRID
```




### COLORFUL_GRID_ACCENT_1 {#COLORFUL-GRID-ACCENT-1}
```
public static int COLORFUL_GRID_ACCENT_1
```




### COLORFUL_GRID_ACCENT_2 {#COLORFUL-GRID-ACCENT-2}
```
public static int COLORFUL_GRID_ACCENT_2
```




### COLORFUL_GRID_ACCENT_3 {#COLORFUL-GRID-ACCENT-3}
```
public static int COLORFUL_GRID_ACCENT_3
```




### COLORFUL_GRID_ACCENT_4 {#COLORFUL-GRID-ACCENT-4}
```
public static int COLORFUL_GRID_ACCENT_4
```




### COLORFUL_GRID_ACCENT_5 {#COLORFUL-GRID-ACCENT-5}
```
public static int COLORFUL_GRID_ACCENT_5
```




### COLORFUL_GRID_ACCENT_6 {#COLORFUL-GRID-ACCENT-6}
```
public static int COLORFUL_GRID_ACCENT_6
```




### COLORFUL_LIST {#COLORFUL-LIST}
```
public static int COLORFUL_LIST
```




### COLORFUL_LIST_ACCENT_1 {#COLORFUL-LIST-ACCENT-1}
```
public static int COLORFUL_LIST_ACCENT_1
```




### COLORFUL_LIST_ACCENT_2 {#COLORFUL-LIST-ACCENT-2}
```
public static int COLORFUL_LIST_ACCENT_2
```




### COLORFUL_LIST_ACCENT_3 {#COLORFUL-LIST-ACCENT-3}
```
public static int COLORFUL_LIST_ACCENT_3
```




### COLORFUL_LIST_ACCENT_4 {#COLORFUL-LIST-ACCENT-4}
```
public static int COLORFUL_LIST_ACCENT_4
```




### COLORFUL_LIST_ACCENT_5 {#COLORFUL-LIST-ACCENT-5}
```
public static int COLORFUL_LIST_ACCENT_5
```




### COLORFUL_LIST_ACCENT_6 {#COLORFUL-LIST-ACCENT-6}
```
public static int COLORFUL_LIST_ACCENT_6
```




### COLORFUL_SHADING {#COLORFUL-SHADING}
```
public static int COLORFUL_SHADING
```




### COLORFUL_SHADING_ACCENT_1 {#COLORFUL-SHADING-ACCENT-1}
```
public static int COLORFUL_SHADING_ACCENT_1
```




### COLORFUL_SHADING_ACCENT_2 {#COLORFUL-SHADING-ACCENT-2}
```
public static int COLORFUL_SHADING_ACCENT_2
```




### COLORFUL_SHADING_ACCENT_3 {#COLORFUL-SHADING-ACCENT-3}
```
public static int COLORFUL_SHADING_ACCENT_3
```




### COLORFUL_SHADING_ACCENT_4 {#COLORFUL-SHADING-ACCENT-4}
```
public static int COLORFUL_SHADING_ACCENT_4
```




### COLORFUL_SHADING_ACCENT_5 {#COLORFUL-SHADING-ACCENT-5}
```
public static int COLORFUL_SHADING_ACCENT_5
```




### COLORFUL_SHADING_ACCENT_6 {#COLORFUL-SHADING-ACCENT-6}
```
public static int COLORFUL_SHADING_ACCENT_6
```




### COMMENT_REFERENCE {#COMMENT-REFERENCE}
```
public static int COMMENT_REFERENCE
```


Lo stile Riferimento dell'annotazione (commento).

### COMMENT_SUBJECT {#COMMENT-SUBJECT}
```
public static int COMMENT_SUBJECT
```




### COMMENT_TEXT {#COMMENT-TEXT}
```
public static int COMMENT_TEXT
```


Lo stile Testo dell'annotazione (commento).

### DARK_LIST {#DARK-LIST}
```
public static int DARK_LIST
```




### DARK_LIST_ACCENT_1 {#DARK-LIST-ACCENT-1}
```
public static int DARK_LIST_ACCENT_1
```




### DARK_LIST_ACCENT_2 {#DARK-LIST-ACCENT-2}
```
public static int DARK_LIST_ACCENT_2
```




### DARK_LIST_ACCENT_3 {#DARK-LIST-ACCENT-3}
```
public static int DARK_LIST_ACCENT_3
```




### DARK_LIST_ACCENT_4 {#DARK-LIST-ACCENT-4}
```
public static int DARK_LIST_ACCENT_4
```




### DARK_LIST_ACCENT_5 {#DARK-LIST-ACCENT-5}
```
public static int DARK_LIST_ACCENT_5
```




### DARK_LIST_ACCENT_6 {#DARK-LIST-ACCENT-6}
```
public static int DARK_LIST_ACCENT_6
```




### DATE {#DATE}
```
public static int DATE
```




### DEFAULT_PARAGRAPH_FONT {#DEFAULT-PARAGRAPH-FONT}
```
public static int DEFAULT_PARAGRAPH_FONT
```


Lo stile Font di paragrafo predefinito.

### DOCUMENT_MAP {#DOCUMENT-MAP}
```
public static int DOCUMENT_MAP
```




### EMAIL_SIGNATURE {#EMAIL-SIGNATURE}
```
public static int EMAIL_SIGNATURE
```




### EMPHASIS {#EMPHASIS}
```
public static int EMPHASIS
```




### ENDNOTE_REFERENCE {#ENDNOTE-REFERENCE}
```
public static int ENDNOTE_REFERENCE
```


Lo stile Riferimento della nota finale.

### ENDNOTE_TEXT {#ENDNOTE-TEXT}
```
public static int ENDNOTE_TEXT
```


Lo stile Testo della nota finale.

### ENVELOPE_ADDRESS {#ENVELOPE-ADDRESS}
```
public static int ENVELOPE_ADDRESS
```


Lo stile Indirizzo della busta.

### ENVELOPE_RETURN {#ENVELOPE-RETURN}
```
public static int ENVELOPE_RETURN
```


Lo stile Ritorno della busta.

### FOLLOWED_HYPERLINK {#FOLLOWED-HYPERLINK}
```
public static int FOLLOWED_HYPERLINK
```




### FOOTER {#FOOTER}
```
public static int FOOTER
```


Lo stile Piè di pagina.

### FOOTNOTE_REFERENCE {#FOOTNOTE-REFERENCE}
```
public static int FOOTNOTE_REFERENCE
```


Lo stile Riferimento della nota a piè di pagina.

### FOOTNOTE_TEXT {#FOOTNOTE-TEXT}
```
public static int FOOTNOTE_TEXT
```


Lo stile Testo della nota a piè di pagina.

### GRID_TABLE_1_LIGHT {#GRID-TABLE-1-LIGHT}
```
public static int GRID_TABLE_1_LIGHT
```


Tabella a griglia 1 chiara

### GRID_TABLE_1_LIGHT_ACCENT_1 {#GRID-TABLE-1-LIGHT-ACCENT-1}
```
public static int GRID_TABLE_1_LIGHT_ACCENT_1
```


Tabella a griglia 1 chiara - Accento 1

### GRID_TABLE_1_LIGHT_ACCENT_2 {#GRID-TABLE-1-LIGHT-ACCENT-2}
```
public static int GRID_TABLE_1_LIGHT_ACCENT_2
```


Tabella a griglia 1 chiara - Accento 2

### GRID_TABLE_1_LIGHT_ACCENT_3 {#GRID-TABLE-1-LIGHT-ACCENT-3}
```
public static int GRID_TABLE_1_LIGHT_ACCENT_3
```


Tabella a griglia 1 chiara - Accento 3

### GRID_TABLE_1_LIGHT_ACCENT_4 {#GRID-TABLE-1-LIGHT-ACCENT-4}
```
public static int GRID_TABLE_1_LIGHT_ACCENT_4
```


Tabella a griglia 1 chiara - Accento 4

### GRID_TABLE_1_LIGHT_ACCENT_5 {#GRID-TABLE-1-LIGHT-ACCENT-5}
```
public static int GRID_TABLE_1_LIGHT_ACCENT_5
```


Tabella a griglia 1 chiara - Accento 5

### GRID_TABLE_1_LIGHT_ACCENT_6 {#GRID-TABLE-1-LIGHT-ACCENT-6}
```
public static int GRID_TABLE_1_LIGHT_ACCENT_6
```


Tabella a griglia 1 chiara - Accento 6

### GRID_TABLE_2 {#GRID-TABLE-2}
```
public static int GRID_TABLE_2
```


Tabella a griglia 2

### GRID_TABLE_2_ACCENT_1 {#GRID-TABLE-2-ACCENT-1}
```
public static int GRID_TABLE_2_ACCENT_1
```


Tabella a griglia 2 - Accento 1

### GRID_TABLE_2_ACCENT_2 {#GRID-TABLE-2-ACCENT-2}
```
public static int GRID_TABLE_2_ACCENT_2
```


Tabella a griglia 2 - Accento 2

### GRID_TABLE_2_ACCENT_3 {#GRID-TABLE-2-ACCENT-3}
```
public static int GRID_TABLE_2_ACCENT_3
```


Tabella a griglia 2 - Accento 3

### GRID_TABLE_2_ACCENT_4 {#GRID-TABLE-2-ACCENT-4}
```
public static int GRID_TABLE_2_ACCENT_4
```


Tabella a griglia 2 - Accento 4

### GRID_TABLE_2_ACCENT_5 {#GRID-TABLE-2-ACCENT-5}
```
public static int GRID_TABLE_2_ACCENT_5
```


Tabella a griglia 2 - Accento 5

### GRID_TABLE_2_ACCENT_6 {#GRID-TABLE-2-ACCENT-6}
```
public static int GRID_TABLE_2_ACCENT_6
```


Tabella a griglia 2 - Accento 6

### GRID_TABLE_3 {#GRID-TABLE-3}
```
public static int GRID_TABLE_3
```


Tabella a griglia 3

### GRID_TABLE_3_ACCENT_1 {#GRID-TABLE-3-ACCENT-1}
```
public static int GRID_TABLE_3_ACCENT_1
```


Tabella a griglia 3 - Accento 1

### GRID_TABLE_3_ACCENT_2 {#GRID-TABLE-3-ACCENT-2}
```
public static int GRID_TABLE_3_ACCENT_2
```


Tabella a griglia 3 - Accento 2

### GRID_TABLE_3_ACCENT_3 {#GRID-TABLE-3-ACCENT-3}
```
public static int GRID_TABLE_3_ACCENT_3
```


Tabella a griglia 3 - Accento 3

### GRID_TABLE_3_ACCENT_4 {#GRID-TABLE-3-ACCENT-4}
```
public static int GRID_TABLE_3_ACCENT_4
```


Tabella a griglia 3 - Accento 4

### GRID_TABLE_3_ACCENT_5 {#GRID-TABLE-3-ACCENT-5}
```
public static int GRID_TABLE_3_ACCENT_5
```


Tabella a griglia 3 - Accento 5

### GRID_TABLE_3_ACCENT_6 {#GRID-TABLE-3-ACCENT-6}
```
public static int GRID_TABLE_3_ACCENT_6
```


Tabella a griglia 3 - Accento 6

### GRID_TABLE_4 {#GRID-TABLE-4}
```
public static int GRID_TABLE_4
```


Tabella a griglia 4

### GRID_TABLE_4_ACCENT_1 {#GRID-TABLE-4-ACCENT-1}
```
public static int GRID_TABLE_4_ACCENT_1
```


Tabella a griglia 4 - Accento 1

### GRID_TABLE_4_ACCENT_2 {#GRID-TABLE-4-ACCENT-2}
```
public static int GRID_TABLE_4_ACCENT_2
```


Tabella a griglia 4 - Accento 2

### GRID_TABLE_4_ACCENT_3 {#GRID-TABLE-4-ACCENT-3}
```
public static int GRID_TABLE_4_ACCENT_3
```


Tabella a griglia 4 - Accento 3

### GRID_TABLE_4_ACCENT_4 {#GRID-TABLE-4-ACCENT-4}
```
public static int GRID_TABLE_4_ACCENT_4
```


Tabella a griglia 4 - Accento 4

### GRID_TABLE_4_ACCENT_5 {#GRID-TABLE-4-ACCENT-5}
```
public static int GRID_TABLE_4_ACCENT_5
```


Tabella a griglia 4 - Accento 5

### GRID_TABLE_4_ACCENT_6 {#GRID-TABLE-4-ACCENT-6}
```
public static int GRID_TABLE_4_ACCENT_6
```


Tabella a griglia 4 - Accento 6

### GRID_TABLE_5_DARK {#GRID-TABLE-5-DARK}
```
public static int GRID_TABLE_5_DARK
```


Tabella a griglia 5 Scuro

### GRID_TABLE_5_DARK_ACCENT_1 {#GRID-TABLE-5-DARK-ACCENT-1}
```
public static int GRID_TABLE_5_DARK_ACCENT_1
```


Tabella a griglia 5 Scuro - Accento 1

### GRID_TABLE_5_DARK_ACCENT_2 {#GRID-TABLE-5-DARK-ACCENT-2}
```
public static int GRID_TABLE_5_DARK_ACCENT_2
```


Tabella a griglia 5 Scuro - Accento 2

### GRID_TABLE_5_DARK_ACCENT_3 {#GRID-TABLE-5-DARK-ACCENT-3}
```
public static int GRID_TABLE_5_DARK_ACCENT_3
```


Tabella a griglia 5 Scuro - Accento 3

### GRID_TABLE_5_DARK_ACCENT_4 {#GRID-TABLE-5-DARK-ACCENT-4}
```
public static int GRID_TABLE_5_DARK_ACCENT_4
```


Tabella a griglia 5 Scuro - Accento 4

### GRID_TABLE_5_DARK_ACCENT_5 {#GRID-TABLE-5-DARK-ACCENT-5}
```
public static int GRID_TABLE_5_DARK_ACCENT_5
```


Tabella a griglia 5 Scuro - Accento 5

### GRID_TABLE_5_DARK_ACCENT_6 {#GRID-TABLE-5-DARK-ACCENT-6}
```
public static int GRID_TABLE_5_DARK_ACCENT_6
```


Tabella a griglia 5 Scuro - Accento 6

### GRID_TABLE_6_COLORFUL {#GRID-TABLE-6-COLORFUL}
```
public static int GRID_TABLE_6_COLORFUL
```


Tabella a griglia 6 Colorato

### GRID_TABLE_6_COLORFUL_ACCENT_1 {#GRID-TABLE-6-COLORFUL-ACCENT-1}
```
public static int GRID_TABLE_6_COLORFUL_ACCENT_1
```


Tabella a griglia 6 Colorata - Accento 1

### GRID_TABLE_6_COLORFUL_ACCENT_2 {#GRID-TABLE-6-COLORFUL-ACCENT-2}
```
public static int GRID_TABLE_6_COLORFUL_ACCENT_2
```


Tabella a griglia 6 Colorata - Accento 2

### GRID_TABLE_6_COLORFUL_ACCENT_3 {#GRID-TABLE-6-COLORFUL-ACCENT-3}
```
public static int GRID_TABLE_6_COLORFUL_ACCENT_3
```


Tabella a griglia 6 Colorata - Accento 3

### GRID_TABLE_6_COLORFUL_ACCENT_4 {#GRID-TABLE-6-COLORFUL-ACCENT-4}
```
public static int GRID_TABLE_6_COLORFUL_ACCENT_4
```


Tabella a griglia 6 Colorata - Accento 4

### GRID_TABLE_6_COLORFUL_ACCENT_5 {#GRID-TABLE-6-COLORFUL-ACCENT-5}
```
public static int GRID_TABLE_6_COLORFUL_ACCENT_5
```


Tabella a griglia 6 Colorata - Accento 5

### GRID_TABLE_6_COLORFUL_ACCENT_6 {#GRID-TABLE-6-COLORFUL-ACCENT-6}
```
public static int GRID_TABLE_6_COLORFUL_ACCENT_6
```


Tabella a griglia 6 Colorata - Accento 6

### GRID_TABLE_7_COLORFUL {#GRID-TABLE-7-COLORFUL}
```
public static int GRID_TABLE_7_COLORFUL
```


Tabella a griglia 7 Colorata

### GRID_TABLE_7_COLORFUL_ACCENT_1 {#GRID-TABLE-7-COLORFUL-ACCENT-1}
```
public static int GRID_TABLE_7_COLORFUL_ACCENT_1
```


Tabella a griglia 7 Colorata - Accento 1

### GRID_TABLE_7_COLORFUL_ACCENT_2 {#GRID-TABLE-7-COLORFUL-ACCENT-2}
```
public static int GRID_TABLE_7_COLORFUL_ACCENT_2
```


Tabella a griglia 7 Colorata - Accento 2

### GRID_TABLE_7_COLORFUL_ACCENT_3 {#GRID-TABLE-7-COLORFUL-ACCENT-3}
```
public static int GRID_TABLE_7_COLORFUL_ACCENT_3
```


Tabella a griglia 7 Colorata - Accento 3

### GRID_TABLE_7_COLORFUL_ACCENT_4 {#GRID-TABLE-7-COLORFUL-ACCENT-4}
```
public static int GRID_TABLE_7_COLORFUL_ACCENT_4
```


Tabella a griglia 7 Colorata - Accento 4

### GRID_TABLE_7_COLORFUL_ACCENT_5 {#GRID-TABLE-7-COLORFUL-ACCENT-5}
```
public static int GRID_TABLE_7_COLORFUL_ACCENT_5
```


Tabella a griglia 7 Colorata - Accento 5

### GRID_TABLE_7_COLORFUL_ACCENT_6 {#GRID-TABLE-7-COLORFUL-ACCENT-6}
```
public static int GRID_TABLE_7_COLORFUL_ACCENT_6
```


Tabella a griglia 7 Colorata - Accento 6

### HASHTAG {#HASHTAG}
```
public static int HASHTAG
```


Lo stile Hashtag.

### HEADER {#HEADER}
```
public static int HEADER
```


Lo stile Header.

### HEADING_1 {#HEADING-1}
```
public static int HEADING_1
```


Lo stile Titolo 1.

### HEADING_2 {#HEADING-2}
```
public static int HEADING_2
```


Lo stile Titolo 2.

### HEADING_3 {#HEADING-3}
```
public static int HEADING_3
```


Lo stile Titolo 3.

### HEADING_4 {#HEADING-4}
```
public static int HEADING_4
```


Lo stile Titolo 4.

### HEADING_5 {#HEADING-5}
```
public static int HEADING_5
```


Lo stile Titolo 5.

### HEADING_6 {#HEADING-6}
```
public static int HEADING_6
```


Lo stile Titolo 6.

### HEADING_7 {#HEADING-7}
```
public static int HEADING_7
```


Lo stile Titolo 7.

### HEADING_8 {#HEADING-8}
```
public static int HEADING_8
```


Lo stile Titolo 8.

### HEADING_9 {#HEADING-9}
```
public static int HEADING_9
```


Lo stile Titolo 9.

### HTML_ACRONYM {#HTML-ACRONYM}
```
public static int HTML_ACRONYM
```




### HTML_ADDRESS {#HTML-ADDRESS}
```
public static int HTML_ADDRESS
```




### HTML_BOTTOM_OF_FORM {#HTML-BOTTOM-OF-FORM}
```
public static int HTML_BOTTOM_OF_FORM
```




### HTML_CITE {#HTML-CITE}
```
public static int HTML_CITE
```




### HTML_CODE {#HTML-CODE}
```
public static int HTML_CODE
```




### HTML_DEFINITION {#HTML-DEFINITION}
```
public static int HTML_DEFINITION
```




### HTML_KEYBOARD {#HTML-KEYBOARD}
```
public static int HTML_KEYBOARD
```




### HTML_PREFORMATTED {#HTML-PREFORMATTED}
```
public static int HTML_PREFORMATTED
```




### HTML_SAMPLE {#HTML-SAMPLE}
```
public static int HTML_SAMPLE
```




### HTML_TOP_OF_FORM {#HTML-TOP-OF-FORM}
```
public static int HTML_TOP_OF_FORM
```




### HTML_TYPEWRITER {#HTML-TYPEWRITER}
```
public static int HTML_TYPEWRITER
```




### HTML_VARIABLE {#HTML-VARIABLE}
```
public static int HTML_VARIABLE
```




### HYPERLINK {#HYPERLINK}
```
public static int HYPERLINK
```


Lo stile Hyperlink.

### INDEX_1 {#INDEX-1}
```
public static int INDEX_1
```




### INDEX_2 {#INDEX-2}
```
public static int INDEX_2
```




### INDEX_3 {#INDEX-3}
```
public static int INDEX_3
```




### INDEX_4 {#INDEX-4}
```
public static int INDEX_4
```




### INDEX_5 {#INDEX-5}
```
public static int INDEX_5
```




### INDEX_6 {#INDEX-6}
```
public static int INDEX_6
```




### INDEX_7 {#INDEX-7}
```
public static int INDEX_7
```




### INDEX_8 {#INDEX-8}
```
public static int INDEX_8
```




### INDEX_9 {#INDEX-9}
```
public static int INDEX_9
```




### INDEX_HEADING {#INDEX-HEADING}
```
public static int INDEX_HEADING
```


Lo stile intestazione indice.

### INTENSE_EMPHASIS {#INTENSE-EMPHASIS}
```
public static int INTENSE_EMPHASIS
```




### INTENSE_QUOTE {#INTENSE-QUOTE}
```
public static int INTENSE_QUOTE
```




### INTENSE_REFERENCE {#INTENSE-REFERENCE}
```
public static int INTENSE_REFERENCE
```




### LIGHT_GRID {#LIGHT-GRID}
```
public static int LIGHT_GRID
```




### LIGHT_GRID_ACCENT_1 {#LIGHT-GRID-ACCENT-1}
```
public static int LIGHT_GRID_ACCENT_1
```




### LIGHT_GRID_ACCENT_2 {#LIGHT-GRID-ACCENT-2}
```
public static int LIGHT_GRID_ACCENT_2
```




### LIGHT_GRID_ACCENT_3 {#LIGHT-GRID-ACCENT-3}
```
public static int LIGHT_GRID_ACCENT_3
```




### LIGHT_GRID_ACCENT_4 {#LIGHT-GRID-ACCENT-4}
```
public static int LIGHT_GRID_ACCENT_4
```




### LIGHT_GRID_ACCENT_5 {#LIGHT-GRID-ACCENT-5}
```
public static int LIGHT_GRID_ACCENT_5
```




### LIGHT_GRID_ACCENT_6 {#LIGHT-GRID-ACCENT-6}
```
public static int LIGHT_GRID_ACCENT_6
```




### LIGHT_LIST {#LIGHT-LIST}
```
public static int LIGHT_LIST
```




### LIGHT_LIST_ACCENT_1 {#LIGHT-LIST-ACCENT-1}
```
public static int LIGHT_LIST_ACCENT_1
```




### LIGHT_LIST_ACCENT_2 {#LIGHT-LIST-ACCENT-2}
```
public static int LIGHT_LIST_ACCENT_2
```




### LIGHT_LIST_ACCENT_3 {#LIGHT-LIST-ACCENT-3}
```
public static int LIGHT_LIST_ACCENT_3
```




### LIGHT_LIST_ACCENT_4 {#LIGHT-LIST-ACCENT-4}
```
public static int LIGHT_LIST_ACCENT_4
```




### LIGHT_LIST_ACCENT_5 {#LIGHT-LIST-ACCENT-5}
```
public static int LIGHT_LIST_ACCENT_5
```




### LIGHT_LIST_ACCENT_6 {#LIGHT-LIST-ACCENT-6}
```
public static int LIGHT_LIST_ACCENT_6
```




### LIGHT_SHADING {#LIGHT-SHADING}
```
public static int LIGHT_SHADING
```




### LIGHT_SHADING_ACCENT_1 {#LIGHT-SHADING-ACCENT-1}
```
public static int LIGHT_SHADING_ACCENT_1
```




### LIGHT_SHADING_ACCENT_2 {#LIGHT-SHADING-ACCENT-2}
```
public static int LIGHT_SHADING_ACCENT_2
```




### LIGHT_SHADING_ACCENT_3 {#LIGHT-SHADING-ACCENT-3}
```
public static int LIGHT_SHADING_ACCENT_3
```




### LIGHT_SHADING_ACCENT_4 {#LIGHT-SHADING-ACCENT-4}
```
public static int LIGHT_SHADING_ACCENT_4
```




### LIGHT_SHADING_ACCENT_5 {#LIGHT-SHADING-ACCENT-5}
```
public static int LIGHT_SHADING_ACCENT_5
```




### LIGHT_SHADING_ACCENT_6 {#LIGHT-SHADING-ACCENT-6}
```
public static int LIGHT_SHADING_ACCENT_6
```




### LINE_NUMBER {#LINE-NUMBER}
```
public static int LINE_NUMBER
```


Lo stile numero di riga.

### LIST {#LIST}
```
public static int LIST
```


Lo stile elenco.

### LIST_2 {#LIST-2}
```
public static int LIST_2
```




### LIST_3 {#LIST-3}
```
public static int LIST_3
```




### LIST_4 {#LIST-4}
```
public static int LIST_4
```




### LIST_5 {#LIST-5}
```
public static int LIST_5
```




### LIST_BULLET {#LIST-BULLET}
```
public static int LIST_BULLET
```


Lo stile elenco puntato.

### LIST_BULLET_2 {#LIST-BULLET-2}
```
public static int LIST_BULLET_2
```




### LIST_BULLET_3 {#LIST-BULLET-3}
```
public static int LIST_BULLET_3
```




### LIST_BULLET_4 {#LIST-BULLET-4}
```
public static int LIST_BULLET_4
```




### LIST_BULLET_5 {#LIST-BULLET-5}
```
public static int LIST_BULLET_5
```




### LIST_CONTINUE {#LIST-CONTINUE}
```
public static int LIST_CONTINUE
```




### LIST_CONTINUE_2 {#LIST-CONTINUE-2}
```
public static int LIST_CONTINUE_2
```




### LIST_CONTINUE_3 {#LIST-CONTINUE-3}
```
public static int LIST_CONTINUE_3
```




### LIST_CONTINUE_4 {#LIST-CONTINUE-4}
```
public static int LIST_CONTINUE_4
```




### LIST_CONTINUE_5 {#LIST-CONTINUE-5}
```
public static int LIST_CONTINUE_5
```




### LIST_NUMBER {#LIST-NUMBER}
```
public static int LIST_NUMBER
```


Lo stile elenco numerato.

### LIST_NUMBER_2 {#LIST-NUMBER-2}
```
public static int LIST_NUMBER_2
```




### LIST_NUMBER_3 {#LIST-NUMBER-3}
```
public static int LIST_NUMBER_3
```




### LIST_NUMBER_4 {#LIST-NUMBER-4}
```
public static int LIST_NUMBER_4
```




### LIST_NUMBER_5 {#LIST-NUMBER-5}
```
public static int LIST_NUMBER_5
```




### LIST_PARAGRAPH {#LIST-PARAGRAPH}
```
public static int LIST_PARAGRAPH
```




### LIST_TABLE_1_LIGHT {#LIST-TABLE-1-LIGHT}
```
public static int LIST_TABLE_1_LIGHT
```


Lista Tabella 1 Chiara

### LIST_TABLE_1_LIGHT_ACCENT_1 {#LIST-TABLE-1-LIGHT-ACCENT-1}
```
public static int LIST_TABLE_1_LIGHT_ACCENT_1
```


Lista Tabella 1 Chiara - Accento 1

### LIST_TABLE_1_LIGHT_ACCENT_2 {#LIST-TABLE-1-LIGHT-ACCENT-2}
```
public static int LIST_TABLE_1_LIGHT_ACCENT_2
```


Lista Tabella 1 Chiara - Accento 2

### LIST_TABLE_1_LIGHT_ACCENT_3 {#LIST-TABLE-1-LIGHT-ACCENT-3}
```
public static int LIST_TABLE_1_LIGHT_ACCENT_3
```


Lista Tabella 1 Chiara - Accento 3

### LIST_TABLE_1_LIGHT_ACCENT_4 {#LIST-TABLE-1-LIGHT-ACCENT-4}
```
public static int LIST_TABLE_1_LIGHT_ACCENT_4
```


Lista Tabella 1 Chiara - Accento 4

### LIST_TABLE_1_LIGHT_ACCENT_5 {#LIST-TABLE-1-LIGHT-ACCENT-5}
```
public static int LIST_TABLE_1_LIGHT_ACCENT_5
```


Lista Tabella 1 Chiara - Accento 5

### LIST_TABLE_1_LIGHT_ACCENT_6 {#LIST-TABLE-1-LIGHT-ACCENT-6}
```
public static int LIST_TABLE_1_LIGHT_ACCENT_6
```


Lista Tabella 1 Chiara - Accento 6

### LIST_TABLE_2 {#LIST-TABLE-2}
```
public static int LIST_TABLE_2
```


Lista Tabella 2

### LIST_TABLE_2_ACCENT_1 {#LIST-TABLE-2-ACCENT-1}
```
public static int LIST_TABLE_2_ACCENT_1
```


Lista Tabella 2 - Accento 1

### LIST_TABLE_2_ACCENT_2 {#LIST-TABLE-2-ACCENT-2}
```
public static int LIST_TABLE_2_ACCENT_2
```


Lista Tabella 2 - Accento 2

### LIST_TABLE_2_ACCENT_3 {#LIST-TABLE-2-ACCENT-3}
```
public static int LIST_TABLE_2_ACCENT_3
```


Lista Tabella 2 - Accento 3

### LIST_TABLE_2_ACCENT_4 {#LIST-TABLE-2-ACCENT-4}
```
public static int LIST_TABLE_2_ACCENT_4
```


Lista Tabella 2 - Accento 4

### LIST_TABLE_2_ACCENT_5 {#LIST-TABLE-2-ACCENT-5}
```
public static int LIST_TABLE_2_ACCENT_5
```


Lista Tabella 2 - Accento 5

### LIST_TABLE_2_ACCENT_6 {#LIST-TABLE-2-ACCENT-6}
```
public static int LIST_TABLE_2_ACCENT_6
```


Lista Tabella 2 - Accento 6

### LIST_TABLE_3 {#LIST-TABLE-3}
```
public static int LIST_TABLE_3
```


Lista Tabella 3

### LIST_TABLE_3_ACCENT_1 {#LIST-TABLE-3-ACCENT-1}
```
public static int LIST_TABLE_3_ACCENT_1
```


Lista Tabella 3 - Accento 1

### LIST_TABLE_3_ACCENT_2 {#LIST-TABLE-3-ACCENT-2}
```
public static int LIST_TABLE_3_ACCENT_2
```


Lista Tabella 3 - Accento 2

### LIST_TABLE_3_ACCENT_3 {#LIST-TABLE-3-ACCENT-3}
```
public static int LIST_TABLE_3_ACCENT_3
```


Lista Tabella 3 - Accento 3

### LIST_TABLE_3_ACCENT_4 {#LIST-TABLE-3-ACCENT-4}
```
public static int LIST_TABLE_3_ACCENT_4
```


Lista Tabella 3 - Accento 4

### LIST_TABLE_3_ACCENT_5 {#LIST-TABLE-3-ACCENT-5}
```
public static int LIST_TABLE_3_ACCENT_5
```


Lista Tabella 3 - Accento 5

### LIST_TABLE_3_ACCENT_6 {#LIST-TABLE-3-ACCENT-6}
```
public static int LIST_TABLE_3_ACCENT_6
```


Elenco Tabella 3 - Accento 6

### LIST_TABLE_4 {#LIST-TABLE-4}
```
public static int LIST_TABLE_4
```


Elenco Tabella 4

### LIST_TABLE_4_ACCENT_1 {#LIST-TABLE-4-ACCENT-1}
```
public static int LIST_TABLE_4_ACCENT_1
```


Elenco Tabella 4 - Accento 1

### LIST_TABLE_4_ACCENT_2 {#LIST-TABLE-4-ACCENT-2}
```
public static int LIST_TABLE_4_ACCENT_2
```


Elenco Tabella 4 - Accento 2

### LIST_TABLE_4_ACCENT_3 {#LIST-TABLE-4-ACCENT-3}
```
public static int LIST_TABLE_4_ACCENT_3
```


Elenco Tabella 4 - Accento 3

### LIST_TABLE_4_ACCENT_4 {#LIST-TABLE-4-ACCENT-4}
```
public static int LIST_TABLE_4_ACCENT_4
```


Elenco Tabella 4 - Accento 4

### LIST_TABLE_4_ACCENT_5 {#LIST-TABLE-4-ACCENT-5}
```
public static int LIST_TABLE_4_ACCENT_5
```


Elenco Tabella 4 - Accento 5

### LIST_TABLE_4_ACCENT_6 {#LIST-TABLE-4-ACCENT-6}
```
public static int LIST_TABLE_4_ACCENT_6
```


Elenco Tabella 4 - Accento 6

### LIST_TABLE_5_DARK {#LIST-TABLE-5-DARK}
```
public static int LIST_TABLE_5_DARK
```


Elenco Tabella 5 Scuro

### LIST_TABLE_5_DARK_ACCENT_1 {#LIST-TABLE-5-DARK-ACCENT-1}
```
public static int LIST_TABLE_5_DARK_ACCENT_1
```


Elenco Tabella 5 Scuro - Accento 1

### LIST_TABLE_5_DARK_ACCENT_2 {#LIST-TABLE-5-DARK-ACCENT-2}
```
public static int LIST_TABLE_5_DARK_ACCENT_2
```


Elenco Tabella 5 Scuro - Accento 2

### LIST_TABLE_5_DARK_ACCENT_3 {#LIST-TABLE-5-DARK-ACCENT-3}
```
public static int LIST_TABLE_5_DARK_ACCENT_3
```


Elenco Tabella 5 Scuro - Accento 3

### LIST_TABLE_5_DARK_ACCENT_4 {#LIST-TABLE-5-DARK-ACCENT-4}
```
public static int LIST_TABLE_5_DARK_ACCENT_4
```


Elenco Tabella 5 Scuro - Accento 4

### LIST_TABLE_5_DARK_ACCENT_5 {#LIST-TABLE-5-DARK-ACCENT-5}
```
public static int LIST_TABLE_5_DARK_ACCENT_5
```


Elenco Tabella 5 Scuro - Accento 5

### LIST_TABLE_5_DARK_ACCENT_6 {#LIST-TABLE-5-DARK-ACCENT-6}
```
public static int LIST_TABLE_5_DARK_ACCENT_6
```


Elenco Tabella 5 Scuro - Accento 6

### LIST_TABLE_6_COLORFUL {#LIST-TABLE-6-COLORFUL}
```
public static int LIST_TABLE_6_COLORFUL
```


Elenco Tabella 6 Colorato

### LIST_TABLE_6_COLORFUL_ACCENT_1 {#LIST-TABLE-6-COLORFUL-ACCENT-1}
```
public static int LIST_TABLE_6_COLORFUL_ACCENT_1
```


Elenco Tabella 6 Colorato - Accento 1

### LIST_TABLE_6_COLORFUL_ACCENT_2 {#LIST-TABLE-6-COLORFUL-ACCENT-2}
```
public static int LIST_TABLE_6_COLORFUL_ACCENT_2
```


Elenco Tabella 6 Colorato - Accento 2

### LIST_TABLE_6_COLORFUL_ACCENT_3 {#LIST-TABLE-6-COLORFUL-ACCENT-3}
```
public static int LIST_TABLE_6_COLORFUL_ACCENT_3
```


Elenco Tabella 6 Colorato - Accento 3

### LIST_TABLE_6_COLORFUL_ACCENT_4 {#LIST-TABLE-6-COLORFUL-ACCENT-4}
```
public static int LIST_TABLE_6_COLORFUL_ACCENT_4
```


Elenco Tabella 6 Colorato - Accento 4

### LIST_TABLE_6_COLORFUL_ACCENT_5 {#LIST-TABLE-6-COLORFUL-ACCENT-5}
```
public static int LIST_TABLE_6_COLORFUL_ACCENT_5
```


Elenco Tabella 6 Colorato - Accento 5

### LIST_TABLE_6_COLORFUL_ACCENT_6 {#LIST-TABLE-6-COLORFUL-ACCENT-6}
```
public static int LIST_TABLE_6_COLORFUL_ACCENT_6
```


Elenco Tabella 6 Colorato - Accento 6

### LIST_TABLE_7_COLORFUL {#LIST-TABLE-7-COLORFUL}
```
public static int LIST_TABLE_7_COLORFUL
```


Elenco Tabella 7 Colorato

### LIST_TABLE_7_COLORFUL_ACCENT_1 {#LIST-TABLE-7-COLORFUL-ACCENT-1}
```
public static int LIST_TABLE_7_COLORFUL_ACCENT_1
```


Elenco Tabella 7 Colorato - Accento 1

### LIST_TABLE_7_COLORFUL_ACCENT_2 {#LIST-TABLE-7-COLORFUL-ACCENT-2}
```
public static int LIST_TABLE_7_COLORFUL_ACCENT_2
```


Elenco Tabella 7 Colorato - Accento 2

### LIST_TABLE_7_COLORFUL_ACCENT_3 {#LIST-TABLE-7-COLORFUL-ACCENT-3}
```
public static int LIST_TABLE_7_COLORFUL_ACCENT_3
```


Elenco Tabella 7 Colorato - Accento 3

### LIST_TABLE_7_COLORFUL_ACCENT_4 {#LIST-TABLE-7-COLORFUL-ACCENT-4}
```
public static int LIST_TABLE_7_COLORFUL_ACCENT_4
```


Elenco Tabella 7 Colorato - Accento 4

### LIST_TABLE_7_COLORFUL_ACCENT_5 {#LIST-TABLE-7-COLORFUL-ACCENT-5}
```
public static int LIST_TABLE_7_COLORFUL_ACCENT_5
```


Elenco Tabella 7 Colorato - Accento 5

### LIST_TABLE_7_COLORFUL_ACCENT_6 {#LIST-TABLE-7-COLORFUL-ACCENT-6}
```
public static int LIST_TABLE_7_COLORFUL_ACCENT_6
```


Elenco Tabella 7 Colorato - Accento 6

### MACRO {#MACRO}
```
public static int MACRO
```




### MEDIUM_GRID_1 {#MEDIUM-GRID-1}
```
public static int MEDIUM_GRID_1
```




### MEDIUM_GRID_1_ACCENT_1 {#MEDIUM-GRID-1-ACCENT-1}
```
public static int MEDIUM_GRID_1_ACCENT_1
```




### MEDIUM_GRID_1_ACCENT_2 {#MEDIUM-GRID-1-ACCENT-2}
```
public static int MEDIUM_GRID_1_ACCENT_2
```




### MEDIUM_GRID_1_ACCENT_3 {#MEDIUM-GRID-1-ACCENT-3}
```
public static int MEDIUM_GRID_1_ACCENT_3
```




### MEDIUM_GRID_1_ACCENT_4 {#MEDIUM-GRID-1-ACCENT-4}
```
public static int MEDIUM_GRID_1_ACCENT_4
```




### MEDIUM_GRID_1_ACCENT_5 {#MEDIUM-GRID-1-ACCENT-5}
```
public static int MEDIUM_GRID_1_ACCENT_5
```




### MEDIUM_GRID_1_ACCENT_6 {#MEDIUM-GRID-1-ACCENT-6}
```
public static int MEDIUM_GRID_1_ACCENT_6
```




### MEDIUM_GRID_2 {#MEDIUM-GRID-2}
```
public static int MEDIUM_GRID_2
```




### MEDIUM_GRID_2_ACCENT_1 {#MEDIUM-GRID-2-ACCENT-1}
```
public static int MEDIUM_GRID_2_ACCENT_1
```




### MEDIUM_GRID_2_ACCENT_2 {#MEDIUM-GRID-2-ACCENT-2}
```
public static int MEDIUM_GRID_2_ACCENT_2
```




### MEDIUM_GRID_2_ACCENT_3 {#MEDIUM-GRID-2-ACCENT-3}
```
public static int MEDIUM_GRID_2_ACCENT_3
```




### MEDIUM_GRID_2_ACCENT_4 {#MEDIUM-GRID-2-ACCENT-4}
```
public static int MEDIUM_GRID_2_ACCENT_4
```




### MEDIUM_GRID_2_ACCENT_5 {#MEDIUM-GRID-2-ACCENT-5}
```
public static int MEDIUM_GRID_2_ACCENT_5
```




### MEDIUM_GRID_2_ACCENT_6 {#MEDIUM-GRID-2-ACCENT-6}
```
public static int MEDIUM_GRID_2_ACCENT_6
```




### MEDIUM_GRID_3 {#MEDIUM-GRID-3}
```
public static int MEDIUM_GRID_3
```




### MEDIUM_GRID_3_ACCENT_1 {#MEDIUM-GRID-3-ACCENT-1}
```
public static int MEDIUM_GRID_3_ACCENT_1
```




### MEDIUM_GRID_3_ACCENT_2 {#MEDIUM-GRID-3-ACCENT-2}
```
public static int MEDIUM_GRID_3_ACCENT_2
```




### MEDIUM_GRID_3_ACCENT_3 {#MEDIUM-GRID-3-ACCENT-3}
```
public static int MEDIUM_GRID_3_ACCENT_3
```




### MEDIUM_GRID_3_ACCENT_4 {#MEDIUM-GRID-3-ACCENT-4}
```
public static int MEDIUM_GRID_3_ACCENT_4
```




### MEDIUM_GRID_3_ACCENT_5 {#MEDIUM-GRID-3-ACCENT-5}
```
public static int MEDIUM_GRID_3_ACCENT_5
```




### MEDIUM_GRID_3_ACCENT_6 {#MEDIUM-GRID-3-ACCENT-6}
```
public static int MEDIUM_GRID_3_ACCENT_6
```




### MEDIUM_LIST_1 {#MEDIUM-LIST-1}
```
public static int MEDIUM_LIST_1
```




### MEDIUM_LIST_1_ACCENT_1 {#MEDIUM-LIST-1-ACCENT-1}
```
public static int MEDIUM_LIST_1_ACCENT_1
```




### MEDIUM_LIST_1_ACCENT_2 {#MEDIUM-LIST-1-ACCENT-2}
```
public static int MEDIUM_LIST_1_ACCENT_2
```




### MEDIUM_LIST_1_ACCENT_3 {#MEDIUM-LIST-1-ACCENT-3}
```
public static int MEDIUM_LIST_1_ACCENT_3
```




### MEDIUM_LIST_1_ACCENT_4 {#MEDIUM-LIST-1-ACCENT-4}
```
public static int MEDIUM_LIST_1_ACCENT_4
```




### MEDIUM_LIST_1_ACCENT_5 {#MEDIUM-LIST-1-ACCENT-5}
```
public static int MEDIUM_LIST_1_ACCENT_5
```




### MEDIUM_LIST_1_ACCENT_6 {#MEDIUM-LIST-1-ACCENT-6}
```
public static int MEDIUM_LIST_1_ACCENT_6
```




### MEDIUM_LIST_2 {#MEDIUM-LIST-2}
```
public static int MEDIUM_LIST_2
```




### MEDIUM_LIST_2_ACCENT_1 {#MEDIUM-LIST-2-ACCENT-1}
```
public static int MEDIUM_LIST_2_ACCENT_1
```




### MEDIUM_LIST_2_ACCENT_2 {#MEDIUM-LIST-2-ACCENT-2}
```
public static int MEDIUM_LIST_2_ACCENT_2
```




### MEDIUM_LIST_2_ACCENT_3 {#MEDIUM-LIST-2-ACCENT-3}
```
public static int MEDIUM_LIST_2_ACCENT_3
```




### MEDIUM_LIST_2_ACCENT_4 {#MEDIUM-LIST-2-ACCENT-4}
```
public static int MEDIUM_LIST_2_ACCENT_4
```




### MEDIUM_LIST_2_ACCENT_5 {#MEDIUM-LIST-2-ACCENT-5}
```
public static int MEDIUM_LIST_2_ACCENT_5
```




### MEDIUM_LIST_2_ACCENT_6 {#MEDIUM-LIST-2-ACCENT-6}
```
public static int MEDIUM_LIST_2_ACCENT_6
```




### MEDIUM_SHADING_1 {#MEDIUM-SHADING-1}
```
public static int MEDIUM_SHADING_1
```




### MEDIUM_SHADING_1_ACCENT_1 {#MEDIUM-SHADING-1-ACCENT-1}
```
public static int MEDIUM_SHADING_1_ACCENT_1
```




### MEDIUM_SHADING_1_ACCENT_2 {#MEDIUM-SHADING-1-ACCENT-2}
```
public static int MEDIUM_SHADING_1_ACCENT_2
```




### MEDIUM_SHADING_1_ACCENT_3 {#MEDIUM-SHADING-1-ACCENT-3}
```
public static int MEDIUM_SHADING_1_ACCENT_3
```




### MEDIUM_SHADING_1_ACCENT_4 {#MEDIUM-SHADING-1-ACCENT-4}
```
public static int MEDIUM_SHADING_1_ACCENT_4
```




### MEDIUM_SHADING_1_ACCENT_5 {#MEDIUM-SHADING-1-ACCENT-5}
```
public static int MEDIUM_SHADING_1_ACCENT_5
```




### MEDIUM_SHADING_1_ACCENT_6 {#MEDIUM-SHADING-1-ACCENT-6}
```
public static int MEDIUM_SHADING_1_ACCENT_6
```




### MEDIUM_SHADING_2 {#MEDIUM-SHADING-2}
```
public static int MEDIUM_SHADING_2
```




### MEDIUM_SHADING_2_ACCENT_1 {#MEDIUM-SHADING-2-ACCENT-1}
```
public static int MEDIUM_SHADING_2_ACCENT_1
```




### MEDIUM_SHADING_2_ACCENT_2 {#MEDIUM-SHADING-2-ACCENT-2}
```
public static int MEDIUM_SHADING_2_ACCENT_2
```




### MEDIUM_SHADING_2_ACCENT_3 {#MEDIUM-SHADING-2-ACCENT-3}
```
public static int MEDIUM_SHADING_2_ACCENT_3
```




### MEDIUM_SHADING_2_ACCENT_4 {#MEDIUM-SHADING-2-ACCENT-4}
```
public static int MEDIUM_SHADING_2_ACCENT_4
```




### MEDIUM_SHADING_2_ACCENT_5 {#MEDIUM-SHADING-2-ACCENT-5}
```
public static int MEDIUM_SHADING_2_ACCENT_5
```




### MEDIUM_SHADING_2_ACCENT_6 {#MEDIUM-SHADING-2-ACCENT-6}
```
public static int MEDIUM_SHADING_2_ACCENT_6
```




### MENTION {#MENTION}
```
public static int MENTION
```


Lo stile Mention.

### MESSAGE_HEADER {#MESSAGE-HEADER}
```
public static int MESSAGE_HEADER
```




### NIL {#NIL}
```
public static int NIL
```


Riservato per uso interno.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Lo stile Normal.

### NORMAL_INDENT {#NORMAL-INDENT}
```
public static int NORMAL_INDENT
```


Lo stile Normal Indent.

### NORMAL_WEB {#NORMAL-WEB}
```
public static int NORMAL_WEB
```




### NOTE_HEADING {#NOTE-HEADING}
```
public static int NOTE_HEADING
```




### NO_LIST {#NO-LIST}
```
public static int NO_LIST
```




### NO_SPACING {#NO-SPACING}
```
public static int NO_SPACING
```




### OUTLINE_LIST_1 {#OUTLINE-LIST-1}
```
public static int OUTLINE_LIST_1
```


Lo stile 1 / a / i.

### OUTLINE_LIST_2 {#OUTLINE-LIST-2}
```
public static int OUTLINE_LIST_2
```


Lo stile 1 / 1.1 / 1.1.1.

### OUTLINE_LIST_3 {#OUTLINE-LIST-3}
```
public static int OUTLINE_LIST_3
```


Lo stile Article / Section.

### PAGE_NUMBER {#PAGE-NUMBER}
```
public static int PAGE_NUMBER
```


Lo stile Page Number.

### PLACEHOLDER_TEXT {#PLACEHOLDER-TEXT}
```
public static int PLACEHOLDER_TEXT
```




### PLAIN_TABLE_1 {#PLAIN-TABLE-1}
```
public static int PLAIN_TABLE_1
```


Tabella Semplice 1

### PLAIN_TABLE_2 {#PLAIN-TABLE-2}
```
public static int PLAIN_TABLE_2
```


Tabella Semplice 2

### PLAIN_TABLE_3 {#PLAIN-TABLE-3}
```
public static int PLAIN_TABLE_3
```


Tabella Semplice 3

### PLAIN_TABLE_4 {#PLAIN-TABLE-4}
```
public static int PLAIN_TABLE_4
```


Tabella Semplice 4

### PLAIN_TABLE_5 {#PLAIN-TABLE-5}
```
public static int PLAIN_TABLE_5
```


Tabella Semplice 5

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```




### QUOTE {#QUOTE}
```
public static int QUOTE
```




### REVISION {#REVISION}
```
public static int REVISION
```




### SALUTATION {#SALUTATION}
```
public static int SALUTATION
```




### SIGNATURE {#SIGNATURE}
```
public static int SIGNATURE
```




### SMART_HYPERLINK {#SMART-HYPERLINK}
```
public static int SMART_HYPERLINK
```


Lo stile SmartHyperlink.

### SMART_LINK {#SMART-LINK}
```
public static int SMART_LINK
```


Lo stile Smart Link.

### STRONG {#STRONG}
```
public static int STRONG
```




### SUBTITLE {#SUBTITLE}
```
public static int SUBTITLE
```




### SUBTLE_EMPHASIS {#SUBTLE-EMPHASIS}
```
public static int SUBTLE_EMPHASIS
```




### SUBTLE_REFERENCE {#SUBTLE-REFERENCE}
```
public static int SUBTLE_REFERENCE
```




### TABLE_3_D_EFFECTS_1 {#TABLE-3-D-EFFECTS-1}
```
public static int TABLE_3_D_EFFECTS_1
```




### TABLE_3_D_EFFECTS_2 {#TABLE-3-D-EFFECTS-2}
```
public static int TABLE_3_D_EFFECTS_2
```




### TABLE_3_D_EFFECTS_3 {#TABLE-3-D-EFFECTS-3}
```
public static int TABLE_3_D_EFFECTS_3
```




### TABLE_CLASSIC_1 {#TABLE-CLASSIC-1}
```
public static int TABLE_CLASSIC_1
```




### TABLE_CLASSIC_2 {#TABLE-CLASSIC-2}
```
public static int TABLE_CLASSIC_2
```




### TABLE_CLASSIC_3 {#TABLE-CLASSIC-3}
```
public static int TABLE_CLASSIC_3
```




### TABLE_CLASSIC_4 {#TABLE-CLASSIC-4}
```
public static int TABLE_CLASSIC_4
```




### TABLE_COLORFUL_1 {#TABLE-COLORFUL-1}
```
public static int TABLE_COLORFUL_1
```




### TABLE_COLORFUL_2 {#TABLE-COLORFUL-2}
```
public static int TABLE_COLORFUL_2
```




### TABLE_COLORFUL_3 {#TABLE-COLORFUL-3}
```
public static int TABLE_COLORFUL_3
```




### TABLE_COLUMNS_1 {#TABLE-COLUMNS-1}
```
public static int TABLE_COLUMNS_1
```




### TABLE_COLUMNS_2 {#TABLE-COLUMNS-2}
```
public static int TABLE_COLUMNS_2
```




### TABLE_COLUMNS_3 {#TABLE-COLUMNS-3}
```
public static int TABLE_COLUMNS_3
```




### TABLE_COLUMNS_4 {#TABLE-COLUMNS-4}
```
public static int TABLE_COLUMNS_4
```




### TABLE_COLUMNS_5 {#TABLE-COLUMNS-5}
```
public static int TABLE_COLUMNS_5
```




### TABLE_CONTEMPORARY {#TABLE-CONTEMPORARY}
```
public static int TABLE_CONTEMPORARY
```




### TABLE_ELEGANT {#TABLE-ELEGANT}
```
public static int TABLE_ELEGANT
```




### TABLE_GRID {#TABLE-GRID}
```
public static int TABLE_GRID
```




### TABLE_GRID_1 {#TABLE-GRID-1}
```
public static int TABLE_GRID_1
```




### TABLE_GRID_2 {#TABLE-GRID-2}
```
public static int TABLE_GRID_2
```




### TABLE_GRID_3 {#TABLE-GRID-3}
```
public static int TABLE_GRID_3
```




### TABLE_GRID_4 {#TABLE-GRID-4}
```
public static int TABLE_GRID_4
```




### TABLE_GRID_5 {#TABLE-GRID-5}
```
public static int TABLE_GRID_5
```




### TABLE_GRID_6 {#TABLE-GRID-6}
```
public static int TABLE_GRID_6
```




### TABLE_GRID_7 {#TABLE-GRID-7}
```
public static int TABLE_GRID_7
```




### TABLE_GRID_8 {#TABLE-GRID-8}
```
public static int TABLE_GRID_8
```




### TABLE_GRID_LIGHT {#TABLE-GRID-LIGHT}
```
public static int TABLE_GRID_LIGHT
```


Tabella Griglia Leggera

### TABLE_LIST_1 {#TABLE-LIST-1}
```
public static int TABLE_LIST_1
```




### TABLE_LIST_2 {#TABLE-LIST-2}
```
public static int TABLE_LIST_2
```




### TABLE_LIST_3 {#TABLE-LIST-3}
```
public static int TABLE_LIST_3
```




### TABLE_LIST_4 {#TABLE-LIST-4}
```
public static int TABLE_LIST_4
```




### TABLE_LIST_5 {#TABLE-LIST-5}
```
public static int TABLE_LIST_5
```




### TABLE_LIST_6 {#TABLE-LIST-6}
```
public static int TABLE_LIST_6
```




### TABLE_LIST_7 {#TABLE-LIST-7}
```
public static int TABLE_LIST_7
```




### TABLE_LIST_8 {#TABLE-LIST-8}
```
public static int TABLE_LIST_8
```




### TABLE_NORMAL {#TABLE-NORMAL}
```
public static int TABLE_NORMAL
```




### TABLE_OF_AUTHORITIES {#TABLE-OF-AUTHORITIES}
```
public static int TABLE_OF_AUTHORITIES
```




### TABLE_OF_FIGURES {#TABLE-OF-FIGURES}
```
public static int TABLE_OF_FIGURES
```


Lo stile Tabella delle Figure.

### TABLE_PROFESSIONAL {#TABLE-PROFESSIONAL}
```
public static int TABLE_PROFESSIONAL
```




### TABLE_SIMPLE_1 {#TABLE-SIMPLE-1}
```
public static int TABLE_SIMPLE_1
```




### TABLE_SIMPLE_2 {#TABLE-SIMPLE-2}
```
public static int TABLE_SIMPLE_2
```




### TABLE_SIMPLE_3 {#TABLE-SIMPLE-3}
```
public static int TABLE_SIMPLE_3
```




### TABLE_SUBTLE_1 {#TABLE-SUBTLE-1}
```
public static int TABLE_SUBTLE_1
```




### TABLE_SUBTLE_2 {#TABLE-SUBTLE-2}
```
public static int TABLE_SUBTLE_2
```




### TABLE_THEME {#TABLE-THEME}
```
public static int TABLE_THEME
```




### TABLE_WEB_1 {#TABLE-WEB-1}
```
public static int TABLE_WEB_1
```




### TABLE_WEB_2 {#TABLE-WEB-2}
```
public static int TABLE_WEB_2
```




### TABLE_WEB_3 {#TABLE-WEB-3}
```
public static int TABLE_WEB_3
```




### TITLE {#TITLE}
```
public static int TITLE
```


Lo stile Title.

### TOA_HEADING {#TOA-HEADING}
```
public static int TOA_HEADING
```




### TOC_1 {#TOC-1}
```
public static int TOC_1
```




### TOC_2 {#TOC-2}
```
public static int TOC_2
```




### TOC_3 {#TOC-3}
```
public static int TOC_3
```




### TOC_4 {#TOC-4}
```
public static int TOC_4
```




### TOC_5 {#TOC-5}
```
public static int TOC_5
```




### TOC_6 {#TOC-6}
```
public static int TOC_6
```




### TOC_7 {#TOC-7}
```
public static int TOC_7
```




### TOC_8 {#TOC-8}
```
public static int TOC_8
```




### TOC_9 {#TOC-9}
```
public static int TOC_9
```




### TOC_HEADING {#TOC-HEADING}
```
public static int TOC_HEADING
```




### UNRESOLVED_MENTION {#UNRESOLVED-MENTION}
```
public static int UNRESOLVED_MENTION
```


Lo stile UnresolvedMention.

### USER {#USER}
```
public static int USER
```


Uno stile definito dall'utente.

### length {#length}
```
public static int length
```


### fromName(String styleIdentifierName) {#fromName-java.lang.String}
```
public static int fromName(String styleIdentifierName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| styleIdentifierName | java.lang.String |  |

**Returns:**
int
### getName(int styleIdentifier) {#getName-int}
```
public static String getName(int styleIdentifier)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| styleIdentifier | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int styleIdentifier) {#toString-int}
```
public static String toString(int styleIdentifier)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| styleIdentifier | int |  |

**Returns:**
java.lang.String
