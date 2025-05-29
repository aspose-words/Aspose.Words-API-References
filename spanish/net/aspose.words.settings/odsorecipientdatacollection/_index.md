---
title: OdsoRecipientDataCollection Class
linktitle: OdsoRecipientDataCollection
articleTitle: OdsoRecipientDataCollection
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.Settings.OdsoRecipientDataCollection, una potente colección tipificada para administrar OdsoRecipientData de manera eficiente en sus aplicaciones.
type: docs
weight: 6770
url: /es/net/aspose.words.settings/odsorecipientdatacollection/
---
## OdsoRecipientDataCollection class

Una colección tipificada de[`OdsoRecipientData`](../odsorecipientdata/)

Para obtener más información, visite el[Combinación de correspondencia e informes](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Artículo de documentación.

```csharp
public class OdsoRecipientDataCollection : IEnumerable<OdsoRecipientData>
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [OdsoRecipientDataCollection](odsorecipientdatacollection/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.settings/odsorecipientdatacollection/count/) { get; } | Obtiene el número de elementos contenidos en la colección. |
| [Item](../../aspose.words.settings/odsorecipientdatacollection/item/) { get; set; } | Obtiene o establece un elemento en esta colección. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.settings/odsorecipientdatacollection/add/)(*[OdsoRecipientData](../odsorecipientdata/)*) | Agrega un objeto al final de esta colección. |
| [Clear](../../aspose.words.settings/odsorecipientdatacollection/clear/)() | Elimina todos los elementos de esta colección. |
| [GetEnumerator](../../aspose.words.settings/odsorecipientdatacollection/getenumerator/)() | Devuelve un objeto enumerador que se puede utilizar para iterar sobre todos los elementos de la colección. |
| [RemoveAt](../../aspose.words.settings/odsorecipientdatacollection/removeat/)(*int*) | Elimina el elemento en el índice especificado. |

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

//Podemos clonar los elementos de esta colección.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// También podemos eliminar elementos individualmente o borrar toda la colección de una vez.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Ver también

* class [OdsoRecipientData](../odsorecipientdata/)
* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)
