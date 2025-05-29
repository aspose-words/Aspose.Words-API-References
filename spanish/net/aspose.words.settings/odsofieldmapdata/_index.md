---
title: OdsoFieldMapData Class
linktitle: OdsoFieldMapData
articleTitle: OdsoFieldMapData
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.OdsoFieldMapData para la asignación perfecta de columnas de datos externos a campos de combinación de documentos predefinidos, mejorando la automatización de sus documentos.
type: docs
weight: 6730
url: /es/net/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class

Especifica cómo se asignará una columna en la fuente de datos externa a los campos de combinación predefinidos dentro del documento.

Para obtener más información, visite el[Combinación de correspondencia e informes](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Artículo de documentación.

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
| [Column](../../aspose.words.settings/odsofieldmapdata/column/) { get; set; } | Especifica el índice basado en cero de la columna dentro de una fuente de datos externa que se asignará al nombre local de un campo MERGEFIELD específico. El valor predeterminado es 0. |
| [MappedName](../../aspose.words.settings/odsofieldmapdata/mappedname/) { get; set; } | Especifica el nombre del campo de combinación predefinido que se asignará al número de columna especificado por el[`Column`](./column/) propiedad dentro de este campo mapping. El valor predeterminado es una cadena vacía. |
| [Name](../../aspose.words.settings/odsofieldmapdata/name/) { get; set; } | Especifica el nombre de la columna dentro de una fuente de datos externa para la columna cuyo índice está especificado por el[`Column`](./column/)propiedad. El valor predeterminado es una cadena vacía. |
| [Type](../../aspose.words.settings/odsofieldmapdata/type/) { get; set; } | Especifica si un campo de combinación de correspondencia determinado se ha asignado o no a una columna en la fuente de datos externa dada. El valor predeterminado esDefault . |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clone](../../aspose.words.settings/odsofieldmapdata/clone/)() | Devuelve un clon profundo de este objeto. |

## Observaciones

Microsoft Word proporciona nombres de campos de combinación predefinidos que permiten insertarlos en un documento, como MERGEFIELD o , en los campos ADDRESSBLOCK o GREETINGLINE. La información especificada en`OdsoFieldMapData` permite mapear una columna en la fuente de datos externa a un único campo de combinación predefinido.

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

* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)
