---
title: OdsoFieldMapDataCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words para .NET
description: OdsoFieldMapDataCollection GetEnumerator método. Devuelve un objeto enumerador que se puede utilizar para iterar sobre todos los elementos de la colección en C#.
type: docs
weight: 60
url: /es/net/aspose.words.settings/odsofieldmapdatacollection/getenumerator/
---
## OdsoFieldMapDataCollection.GetEnumerator method

Devuelve un objeto enumerador que se puede utilizar para iterar sobre todos los elementos de la colección.

```csharp
public IEnumerator<OdsoFieldMapData> GetEnumerator()
```

## Ejemplos

Muestra cómo acceder a la colección de datos que asigna columnas de origen de datos para fusionar campos.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Esta colección define cómo una combinación de correspondencia asignará columnas de una fuente de datos
// a los campos predefinidos MERGEFIELD, ADDRESSBLOCK y GREETINGLINE.
OdsoFieldMapDataCollection dataCollection = doc.MailMergeSettings.Odso.FieldMapDatas;
Assert.AreEqual(30, dataCollection.Count);

using (IEnumerator<OdsoFieldMapData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Field map data index {index++}, type \"{enumerator.Current.Type}\":");

        Console.WriteLine(
            enumerator.Current.Type != OdsoFieldMappingType.Null
                ? $"\tColumn \"{enumerator.Current.Name}\", number {enumerator.Current.Column} mapped to merge field \"{enumerator.Current.MappedName}\"."
                : "\tNo valid column to field mapping data present.");
    }
}

// Clona los elementos de esta colección.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Utiliza los elementos del método "RemoveAt" individualmente por índice.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Utilice el método "Borrar" para borrar toda la colección a la vez.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Ver también

* class [OdsoFieldMapData](../../odsofieldmapdata/)
* class [OdsoFieldMapDataCollection](../)
* espacio de nombres [Aspose.Words.Settings](../../../aspose.words.settings/)
* asamblea [Aspose.Words](../../../)
