---
title: OdsoFieldMappingType Enum
linktitle: OdsoFieldMappingType
articleTitle: OdsoFieldMappingType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.OdsoFieldMappingType para una eficiente asignación de campos de combinación de correspondencia a fuentes de datos externas. ¡Mejore la automatización de sus documentos hoy mismo!
type: docs
weight: 6750
url: /es/net/aspose.words.settings/odsofieldmappingtype/
---
## OdsoFieldMappingType enumeration

Especifica los tipos posibles utilizados para indicar si un campo de combinación de correspondencia determinado se ha asignado a una columna en la fuente de datos externa dada.

```csharp
public enum OdsoFieldMappingType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Column | `0` | Especifica que el campo de combinación de correspondencia se ha asignado a una columna en la fuente de datos externa indicada. |
| Null | `1` | Especifica que el campo de combinación de correspondencia no se ha asignado a una columna en la fuente de datos externa dada. |
| Default | `1` | Es igual aNull . |

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

* property [Type](../odsofieldmapdata/type/)
* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)
