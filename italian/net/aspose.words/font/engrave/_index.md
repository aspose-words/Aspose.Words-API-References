---
title: Font.Engrave
linktitle: Engrave
articleTitle: Engrave
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font Engrave. Formatta facilmente i font per un elegante effetto inciso, esaltando la raffinatezza e l'appeal del tuo design.
type: docs
weight: 120
url: /it/net/aspose.words/font/engrave/
---
## Font.Engrave property

Vero se il font è formattato come inciso.

```csharp
public bool Engrave { get; set; }
```

## Esempi

Mostra come applicare effetti di incisione/rilievo al testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// Di seguito sono riportati due modi per utilizzare le ombre per applicare un effetto 3D al testo.
// 1 - Incidere il testo in modo che sembri che le lettere siano affondate nella pagina:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - Stampa il testo in rilievo per far sembrare che le lettere escano dalla pagina:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
