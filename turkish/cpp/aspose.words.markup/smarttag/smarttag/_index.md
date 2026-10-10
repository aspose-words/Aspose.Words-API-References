---
title: "Aspose::Words::Markup::SmartTag::SmartTag yapıcı"
linktitle: "SmartTag"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::SmartTag::SmartTag yapıcı. C++'ta SmartTag sınıfının yeni bir örneğini başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.markup/smarttag/smarttag/
---
## SmartTag::SmartTag constructor


[SmartTag](../) sınıfının yeni bir örneğini başlatır.

```cpp
Aspose::Words::Markup::SmartTag::SmartTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doküman | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Sahip belge. |
## Açıklamalar


Yeni bir düğüm oluşturduğunuzda, düğümün ait olduğu belgeyi belirtmeniz gerekir. Bir düğüm, listeler ve stiller gibi belge genelindeki yapılara bağlı olduğu için belge olmadan var olamaz. Bir düğüm her zaman bir belgeye ait olsa da, belge ağacının bir parçası olup olmayabilir.

Bir düğüm oluşturulduğunda, bir belgeye aittir, ancak henüz belge ağacının bir parçası değildir ve [ParentNode](../../../aspose.words/node/get_parentnode/) null'dur. Bir düğümü belgeye eklemek için, üst düğüm üzerindeki [InsertAfter1()</see> veya <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) metodlarını kullanın.

## Ayrıca Bakınız

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [SmartTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
