---
title: CompositeNode.HasChildNodes
linktitle: HasChildNodes
articleTitle: HasChildNodes
second_title: .NET için Aspose.Words
description: CompositeNode'un HasChildNodes özelliğine sahip alt düğümleri olup olmadığını keşfedin. Verimli düğüm yönetimi için bu temel özellik ile kodlamanızı basitleştirin.
type: docs
weight: 30
url: /tr/net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa.

```csharp
public bool HasChildNodes { get; }
```

## Örnekler

İki tablodaki satırların nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Aşağıda bir belgeden tablo almanın iki yolu bulunmaktadır.
// 1 - Bir Body düğümünün "Tablolar" koleksiyonundan:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - "GetChild" metodunu kullanarak:
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Mevcut tablodaki tüm satırları bir sonrakine ekle.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Boş tablo kabını kaldır.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Ayrıca bakınız

* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
