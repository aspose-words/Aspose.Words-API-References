---
title: MailMerge.RestartListsAtEachSection
linktitle: RestartListsAtEachSection
articleTitle: RestartListsAtEachSection
second_title: Aspose.Words para .NET
description: Descubra la propiedad RestartListsAtEachSection de MailMerge: la lista de control se restablece en cada sección para una combinación de correspondencia fluida. ¡Mejore la precisión de sus documentos hoy mismo!
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

Muestra cómo controlar si la numeración de listas se reinicia o no en cada sección cuando se realiza la combinación de correspondencia.

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
