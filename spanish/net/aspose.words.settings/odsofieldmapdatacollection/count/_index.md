---
title: OdsoFieldMapDataCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words para .NET
description: Descubra la propiedad Count de OdsoFieldMapDataCollection para recuperar eficientemente el número total de elementos de su colección. ¡Optimice la gestión de sus datos hoy mismo!
type: docs
weight: 20
url: /es/net/aspose.words.settings/odsofieldmapdatacollection/count/
---
## OdsoFieldMapDataCollection.Count property

Obtiene el número de elementos contenidos en la colección.

```csharp
public int Count { get; }
```

## Ejemplos

Muestra cómo acceder a la colección de datos que asigna columnas de fuente de datos a campos de combinación.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Esta colección define cómo una combinación de correspondencia asignará columnas de una fuente de datos
// a los campos MERGEFIELD, ADDRESSBLOCK y GREETINGLINE predefinidos.
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

// Clonar los elementos de esta colección.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Utilice el método "RemoveAt" para eliminar elementos individualmente por índice.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Utilice el método "Borrar" para borrar toda la colección de una vez.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Ver también

* class [OdsoFieldMapDataCollection](../)
* espacio de nombres [Aspose.Words.Settings](../../../aspose.words.settings/)
* asamblea [Aspose.Words](../../../)
