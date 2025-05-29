---
title: ListCollection.AddSingleLevelList
linktitle: AddSingleLevelList
articleTitle: AddSingleLevelList
second_title: Aspose.Words para .NET
description: Cree y agregue sin esfuerzo una lista de un solo nivel a su documento con el método ListCollection AddSingleLevelList, mejorando la organización y la claridad.
type: docs
weight: 60
url: /es/net/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection.AddSingleLevelList method

Crea una nueva lista de un solo nivel basada en la plantilla predefinida y la agrega a la colección de listas en el documento.

```csharp
public List AddSingleLevelList(ListTemplate listTemplate)
```

## Ejemplos

Muestra cómo crear una nueva lista de un solo nivel basada en la plantilla predefinida.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ListCollection listCollection = doc.Lists;

// Crea la lista con viñetas a partir de la plantilla BulletCircle.
List bulletedList = listCollection.AddSingleLevelList(ListTemplate.BulletCircle);

// Escribe la lista con viñetas en el documento resultante.
builder.Writeln("Bulleted list starts below:");
builder.ListFormat.List = bulletedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Crea la lista numerada a partir de la plantilla NumberUppercaseLetterDot.
List numberedList = listCollection.AddSingleLevelList(ListTemplate.NumberUppercaseLetterDot);

// Escribe la lista numerada en el documento resultante.
builder.Writeln("Numbered list starts below:");
builder.ListFormat.List = numberedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Save(ArtifactsDir + "Lists.AddSingleLevelList.docx");
```

### Ver también

* class [List](../../list/)
* enum [ListTemplate](../../listtemplate/)
* class [ListCollection](../)
* espacio de nombres [Aspose.Words.Lists](../../../aspose.words.lists/)
* asamblea [Aspose.Words](../../../)
