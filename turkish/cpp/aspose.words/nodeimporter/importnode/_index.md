---
title: "Aspose::Words::NodeImporter::ImportNode metodu"
linktitle: "ImportNode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::NodeImporter::ImportNode metodu. C++'ta bir belgeden diğerine bir düğüm aktarır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/nodeimporter/importnode/
---
## NodeImporter::ImportNode method


Bir belgeden diğerine bir düğüm ithal eder.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeImporter::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Aktarılacak düğüm. |
| isImportChildren | bool | **true** tüm alt düğümleri özyinelemeli olarak içe aktarmak için; aksi takdirde **false**. |

### ReturnValue

Kopyalanmış, içe aktarılmış düğüm. Düğüm hedef belgeye aittir, ancak ebeveyni yoktur.
## Açıklamalar


Bir düğümü içe aktarmak, içe aktaran belgeye ait kaynak düğümün bir kopyasını oluşturur. Döndürülen düğümün ebeveyni yoktur. Kaynak düğüm, orijinal belgede değiştirilmez veya kaldırılmaz.

Başka bir belgeden bir düğüm bu belgeye eklenebilmeden önce, içe aktarılması gerekir. İçe aktarma sırasında, stillere ve listelere referanslar gibi belgeye özgü özellikler orijinalden içe aktaran belgeye çevrilir. Düğüm içe aktarıldıktan sonra, belge içinde uygun konuma [InsertBefore1()</see> veya <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../) kullanılarak eklenebilir.

Kaynak düğüm zaten hedef belgeye aitse, sadece kaynak düğümün derin bir kopyası oluşturulur.

## Ayrıca Bakınız

* Class [Node](../../node/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
