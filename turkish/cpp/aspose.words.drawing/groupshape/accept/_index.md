---
title: "Aspose::Words::Drawing::GroupShape::Accept yöntemi"
linktitle: "Accept"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::GroupShape::Accept yöntemi. C++'ta bir ziyaretçiyi kabul eder."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.drawing/groupshape/accept/
---
## GroupShape::Accept method


Bir ziyaretçiyi kabul eder.

```cpp
bool Aspose::Words::Drawing::GroupShape::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ziyaretçi | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Düğümleri ziyaret edecek ziyaretçi. |

### ReturnValue

Tüm düğümler ziyaret edildiyse true; tüm düğümler ziyaret edilmeden önce [DocumentVisitor](../../../aspose.words/documentvisitor/) işlemi durdurduysa false.
## Açıklamalar


Bu düğüm ve tüm alt düğümlerini yineleyerek dolaşır. Her düğüm, [DocumentVisitor](../../../aspose.words/documentvisitor/) üzerindeki ilgili yöntemi çağırır.

Daha fazla bilgi için Visitor tasarım desenine bakın.

## Ayrıca Bakınız

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [GroupShape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
