---
title: OdsoRecipientData Class
linktitle: OdsoRecipientData
articleTitle: OdsoRecipientData
second_title: Aspose.Words para .NET
description: Aspose.Words.Settings.OdsoRecipientData clase. Representa información sobre un único registro dentro de una fuente de datos externa que se excluirá de la combinación de correspondencia en C#.
type: docs
weight: 5930
url: /es/net/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class

Representa información sobre un único registro dentro de una fuente de datos externa que se excluirá de la combinación de correspondencia.

Para obtener más información, visite el[Combinación de correspondencia e informes](https://docs.aspose.com/words/net/mail-merge-and-reporting/) artículo de documentación.

```csharp
public class OdsoRecipientData
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [OdsoRecipientData](odsorecipientdata/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Active](../../aspose.words.settings/odsorecipientdata/active/) { get; set; } | Especifica si el registro de la fuente de datos se importará a un documento cuando se realice la combinación de correspondencia. El valor predeterminado es`verdadero` . |
| [Column](../../aspose.words.settings/odsorecipientdata/column/) { get; set; } | Especifica la columna dentro de la fuente de datos que contiene datos únicos para el registro actual. El valor predeterminado es 0. |
| [Hash](../../aspose.words.settings/odsorecipientdata/hash/) { get; set; } | Representa el código hash de este registro. A veces se utiliza Microsoft Word[`Hash`](./hash/) de un registro completo en lugar de un[`UniqueTag`](./uniquetag/) valor. El valor predeterminado es 0. |
| [UniqueTag](../../aspose.words.settings/odsorecipientdata/uniquetag/) { get; set; } | Especifica el contenido de un registro determinado en la columna que contiene datos únicos. El valor predeterminado es`nulo` . |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clone](../../aspose.words.settings/odsorecipientdata/clone/)() | Devuelve un clon profundo de este objeto. |

## Observaciones

Si un registro se fusionará en un documento combinado, entonces no se necesita información sobre ese registro. Sin embargo, si un registro determinado no se fusionará en un documento combinado, entonces el valor de la clave única para ese registro se almacenará en el[`UniqueTag`](./uniquetag/)propiedad de este objeto para indicar esta exclusión.

## Ejemplos

Muestra cómo acceder a la colección de datos que designa qué registros de origen de datos de combinación excluirá una combinación de correspondencia.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

OdsoRecipientDataCollection dataCollection = doc.MailMergeSettings.Odso.RecipientDatas;

Assert.AreEqual(70, dataCollection.Count);

using (IEnumerator<OdsoRecipientData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine(
            $"Odso recipient data index {index++} will {(enumerator.Current.Active ? "" : "not ")}be imported upon mail merge.");
        Console.WriteLine($"\tColumn #{enumerator.Current.Column}");
        Console.WriteLine($"\tHash code: {enumerator.Current.Hash}");
        Console.WriteLine($"\tContents array length: {enumerator.Current.UniqueTag.Length}");
    }
}

// Podemos clonar los elementos de esta colección.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// También podemos eliminar elementos individualmente o borrar toda la colección a la vez.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Ver también

* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)
