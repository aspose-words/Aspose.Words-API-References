---
title: OdsoFieldMapData Class
linktitle: OdsoFieldMapData
articleTitle: OdsoFieldMapData
second_title: Aspose.Words para .NET
description: Aspose.Words.Settings.OdsoFieldMapData clase. Especifica cómo se asignará una columna de la fuente de datos externa a los campos de combinación predefinidos dentro del documento en C#.
type: docs
weight: 5900
url: /es/net/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class

Especifica cómo se asignará una columna de la fuente de datos externa a los campos de combinación predefinidos dentro del documento.

Para obtener más información, visite el[Combinación de correspondencia e informes](https://docs.aspose.com/words/net/mail-merge-and-reporting/) artículo de documentación.

```csharp
public class OdsoFieldMapData
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [OdsoFieldMapData](odsofieldmapdata/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Column](../../aspose.words.settings/odsofieldmapdata/column/) { get; set; } | Especifica el índice de base cero de la columna dentro de una fuente de datos externa que se asignará al nombre local de un campo MERGEFIELD específico. El valor predeterminado es 0. |
| [MappedName](../../aspose.words.settings/odsofieldmapdata/mappedname/) { get; set; } | Especifica el nombre del campo de combinación predefinido que se asignará al número de columna especificado por[`Column`](./column/) propiedad dentro de esta asignación de campos. El valor predeterminado es una cadena vacía. |
| [Name](../../aspose.words.settings/odsofieldmapdata/name/) { get; set; } | Especifica el nombre de la columna dentro de una fuente de datos externa para la columna cuyo índice está especificado por el[`Column`](./column/)propiedad. El valor predeterminado es una cadena vacía. |
| [Type](../../aspose.words.settings/odsofieldmapdata/type/) { get; set; } | Especifica si un campo de combinación de correspondencia determinado se ha asignado a una columna en la fuente de datos externa determinada o no. El valor predeterminado esDefault . |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clone](../../aspose.words.settings/odsofieldmapdata/clone/)() | Devuelve un clon profundo de este objeto. |

## Observaciones

Microsoft Word proporciona algunos nombres de campos de combinación predefinidos que permiten insertar en un documento como MERGEFIELD o en los campos ADDRESSBLOCK o GREETINGLINE. La información especificada en`OdsoFieldMapData` permite asignar una columna en la fuente de datos externa a un único campo de combinación predefinido.

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

* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)
