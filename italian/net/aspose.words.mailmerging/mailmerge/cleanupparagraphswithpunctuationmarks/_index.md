---
title: MailMerge.CleanupParagraphsWithPunctuationMarks
second_title: Aspose.Words per .NET API Reference
description: MailMerge proprietà. Ottiene o imposta un valore che indica se i paragrafi con segni di punteggiatura sono considerati vuoti e devono essere rimossi seRemoveEmptyParagraphs lopzione è specificata.
type: docs
weight: 20
url: /it/net/aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/
---
## MailMerge.CleanupParagraphsWithPunctuationMarks property

Ottiene o imposta un valore che indica se i paragrafi con segni di punteggiatura sono considerati vuoti e devono essere rimossi seRemoveEmptyParagraphs l'opzione è specificata.

```csharp
public bool CleanupParagraphsWithPunctuationMarks { get; set; }
```

### Osservazioni

Il valore predefinito è`VERO` .

Ecco l'elenco completo dei segni di punteggiatura pulibili:

* !
* ,
* .
* :
* ;
* ?
* ¡
* ¿

### Esempi

Mostra come rimuovere i paragrafi con segni di punteggiatura dopo un'operazione di stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldMergeField mergeFieldOption1 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_1");
mergeFieldOption1.FieldName = "Option_1";

builder.Write(punctuationMark);

FieldMergeField mergeFieldOption2 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_2");
mergeFieldOption2.FieldName = "Option_2";

// Configura la proprietà "CleanupOptions" per rimuovere eventuali paragrafi vuoti che questa stampa unione creerebbe.
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyParagraphs;

// Impostando la proprietà "CleanupParagraphsWithPunctuationMarks" su "true" verranno conteggiati anche i paragrafi
// con i segni di punteggiatura vuoti e l'operazione di stampa unione rimuoverà anche questi.
// Impostazione della proprietà "CleanupParagraphsWithPunctuationMarks" su "false"
// rimuoverà i paragrafi vuoti, ma non quelli con segni di punteggiatura.
// Questo è un elenco di segni di punteggiatura che riguardano questa proprietà: "!", ",", ".", ":", ";", "?", "¡", "¿".
doc.MailMerge.CleanupParagraphsWithPunctuationMarks = cleanupParagraphsWithPunctuationMarks;

doc.MailMerge.Execute(new[] { "Option_1", "Option_2" }, new object[] { null, null });

doc.Save(ArtifactsDir + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)


