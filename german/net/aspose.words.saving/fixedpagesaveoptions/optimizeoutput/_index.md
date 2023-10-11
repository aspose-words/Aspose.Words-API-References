---
title: FixedPageSaveOptions.OptimizeOutput
second_title: Aspose.Words für .NET-API-Referenz
description: FixedPageSaveOptions eigendom. Flag gibt an ob es zur Optimierung der Ausgabe erforderlich ist. Wenn dieses Flag gesetzt ist werden redundante verschachtelte Leinwände und leere Leinwände entfernt auch benachbarte Glyphen mit derselben Formatierung werden verkettet. Hinweis Die Genauigkeit der Inhaltsanzeige kann beeinträchtigt werden wenn Diese Eigenschaft ist auf festgelegtWAHR . Standard istFALSCH .
type: docs
weight: 50
url: /de/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

Flag gibt an, ob es zur Optimierung der Ausgabe erforderlich ist. Wenn dieses Flag gesetzt ist, werden redundante verschachtelte Leinwände und leere Leinwände entfernt, auch benachbarte Glyphen mit derselben Formatierung werden verkettet. Hinweis: Die Genauigkeit der Inhaltsanzeige kann beeinträchtigt werden, wenn Diese Eigenschaft ist auf festgelegt`WAHR` . Standard ist`FALSCH` .

```csharp
public virtual bool OptimizeOutput { get; set; }
```

### Beispiele

Zeigt, wie Dokumentobjekte beim Speichern im XPS optimiert werden.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// Erstellen Sie ein „XpsSaveOptions“-Objekt, um es an die „Save“-Methode des Dokuments zu übergeben
// um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
XpsSaveOptions saveOptions = new XpsSaveOptions();

// Setzen Sie die Eigenschaft „OptimizeOutput“ auf „true“, um Maßnahmen wie das Entfernen verschachtelter oder leerer Leinwände zu ergreifen
// und Verketten benachbarter Läufe mit identischer Formatierung, um den Inhalt des Ausgabedokuments zu optimieren.
// Dies kann sich auf das Erscheinungsbild des Dokuments auswirken.
// Setzen Sie die Eigenschaft „OptimizeOutput“ auf „false“, um das Dokument normal zu speichern.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### Siehe auch

* class [FixedPageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* Montage [Aspose.Words](../../../)


