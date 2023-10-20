---
title: MailMerge.RestartListsAtEachSection
linktitle: RestartListsAtEachSection
articleTitle: RestartListsAtEachSection
second_title: Aspose.Words para .NET
description: MailMerge RestartListsAtEachSection propiedad. Obtiene o establece un valor que indica si las listas se reinician en cada sección después de ejecutar una combinación de correspondencia en C#.
type: docs
weight: 110
url: /es/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

Obtiene o establece un valor que indica si las listas se reinician en cada sección después de ejecutar una combinación de correspondencia.

```csharp
public bool RestartListsAtEachSection { get; set; }
```

## Observaciones

El valor predeterminado es`verdadero` .

## Ejemplos

Muestra cómo controlar si se reinicia o no la numeración de listas en cada sección cuando se realiza la combinación de correspondencia.

```csharp
Document doc = new Document(MyDir + "Section breaks with numbering.docx");

doc.MailMerge.RestartListsAtEachSection = false;
doc.MailMerge.Execute(new string[0], new object[0]);

doc.Save(ArtifactsDir + "MailMerge.RestartListsAtEachSection.pdf");
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
