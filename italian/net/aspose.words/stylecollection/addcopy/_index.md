---
title: StyleCollection.AddCopy
linktitle: AddCopy
articleTitle: AddCopy
second_title: Aspose.Words per .NET
description: StyleCollection AddCopy metodo. Copia uno stile in questa raccolta in C#.
type: docs
weight: 70
url: /it/net/aspose.words/stylecollection/addcopy/
---
## StyleCollection.AddCopy method

Copia uno stile in questa raccolta.

```csharp
public Style AddCopy(Style style)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| style | Style | Stile da copiare. |

### Valore di ritorno

Stile copiato pronto per l'uso.

## Osservazioni

Lo stile da copiare può appartenere allo stesso documento oppure a documenti diversi.

Lo stile collegato viene copiato.

Questo metodo non copia gli stili di base.

Se la raccolta contiene già uno stile con lo stesso nome, il nuovo nome viene generato automaticamente aggiungendo il suffisso "_number" a partire da 0, ad esempio "Normal_0", "Intestazione 1_1" ecc. Usa[`Name`](../../style/name/) setter per cambiare il nome dello stile importato.

## Esempi

Mostra come importare uno stile da un documento in un documento diverso.

```csharp
Document srcDoc = new Document();

// Crea uno stile personalizzato per il documento di origine.
Style srcStyle = srcDoc.Styles.Add(StyleType.Paragraph, "MyStyle");
srcStyle.Font.Color = Color.Red;

// Importa lo stile personalizzato del documento di origine nel documento di destinazione.
Document dstDoc = new Document();
Style newStyle = dstDoc.Styles.AddCopy(srcStyle);

// Lo stile importato ha un aspetto identico al suo stile di origine.
Assert.AreEqual("MyStyle", newStyle.Name);
Assert.AreEqual(Color.Red.ToArgb(), newStyle.Font.Color.ToArgb());
```

Mostra come clonare lo stile di un documento.

```csharp
Document doc = new Document();

// Il metodo AddCopy crea una copia dello stile specificato e
// genera automaticamente un nuovo nome per lo stile, ad esempio "Intestazione 1_0".
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

// Utilizza la proprietà "Nome" dello stile per modificare il nome identificativo dello stile.
newStyle.Name = "My Heading 1";

// Il nostro documento ora ha due stili identici con nomi diversi.
// La modifica delle impostazioni di uno degli stili non influisce sull'altro.
newStyle.Font.Color = Color.Red;

Assert.AreEqual("My Heading 1", newStyle.Name);
Assert.AreEqual("Heading 1", doc.Styles["Heading 1"].Name);

Assert.AreEqual(doc.Styles["Heading 1"].Type, newStyle.Type);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Name, newStyle.Font.Name);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Size, newStyle.Font.Size);
Assert.AreNotEqual(doc.Styles["Heading 1"].Font.Color, newStyle.Font.Color);
```

### Guarda anche

* class [Style](../../style/)
* class [StyleCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
