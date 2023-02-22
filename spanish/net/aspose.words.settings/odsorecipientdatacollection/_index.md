---
title: Class OdsoRecipientDataCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Settings.OdsoRecipientDataCollection clase. Una colección escrita deOdsoRecipientData
type: docs
weight: 5640
url: /es/net/aspose.words.settings/odsorecipientdatacollection/
---
## OdsoRecipientDataCollection class

Una colección escrita de[`OdsoRecipientData`](../odsorecipientdata/)

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
| [Count](../../aspose.words.settings/odsorecipientdatacollection/count/) { get; } | Obtiene el número de elementos que contiene la colección. |
| [Item](../../aspose.words.settings/odsorecipientdatacollection/item/) { get; set; } | Obtiene o establece un elemento de esta colección. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.settings/odsorecipientdatacollection/add/)(OdsoRecipientData) | Agrega un objeto al final de esta colección. |
| [Clear](../../aspose.words.settings/odsorecipientdatacollection/clear/)() | Elimina todos los elementos de esta colección. |
| [GetEnumerator](../../aspose.words.settings/odsorecipientdatacollection/getenumerator/)() | Devuelve un objeto enumerador que se puede usar para iterar sobre todos los elementos de la colección. |
| [RemoveAt](../../aspose.words.settings/odsorecipientdatacollection/removeat/)(int) | Elimina el elemento en el índice especificado. |

### Ejemplos

Muestra cómo acceder a la colección de datos que designa qué registros de origen de datos combinados excluirá una combinación de correspondencia.

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

* class [OdsoRecipientData](../odsorecipientdata/)
* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)


