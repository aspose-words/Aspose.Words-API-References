---
title: OdsoFieldMapData.Column
second_title: Referencia de API de Aspose.Words para .NET
description: OdsoFieldMapData propiedad. Especifica el índice de base cero de la columna dentro de una fuente de datos externa que se asignará al nombre local de un campo MERGEFIELD específico. El valor predeterminado es 0.
type: docs
weight: 20
url: /es/net/aspose.words.settings/odsofieldmapdata/column/
---
## OdsoFieldMapData.Column property

Especifica el índice de base cero de la columna dentro de una fuente de datos externa que se asignará al nombre local de un campo MERGEFIELD específico. El valor predeterminado es 0.

```csharp
public int Column { get; set; }
```

### Ejemplos

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

* class [OdsoFieldMapData](../)
* espacio de nombres [Aspose.Words.Settings](../../odsofieldmapdata/)
* asamblea [Aspose.Words](../../../)


