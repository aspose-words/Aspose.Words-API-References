---
title: "Aspose::Words::DocumentVisitor::VisitFieldStart yöntemi"
linktitle: "VisitFieldStart"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentVisitor::VisitFieldStart yöntemi. C++'ta belgede bir alan başladığında çağrılır."
type: docs
weight: 23000
url: /tr/cpp/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor::VisitFieldStart method


Belge içinde bir alan başladığında çağrılır.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldStart(System::SharedPtr<Aspose::Words::Fields::FieldStart> fieldStart)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldStart | System::SharedPtr\<Aspose::Words::Fields::FieldStart\> | Ziyaret edilen nesne. |

### ReturnValue

Sıralamayı nasıl devam ettireceğini belirten bir [VisitorAction](../../visitoraction/) değeri.
## Açıklamalar


Word belgesindeki bir alan, bir alan kodu ve alan değerinden oluşur.

Örneğin, sayfa numarasını gösteren bir alan aşağıdaki gibi temsil edilebilir:

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

Alan ayırıcı, belge içinde alan kodunu alan değerinden ayırır. Bazı alanların yalnızca alan kodu olduğunu ve alan ayırıcı ve alan değerine sahip olmadığını unutmayın.

[Fields](../../../aspose.words.fields/) can be nested.

## Ayrıca Bakınız

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldStart](../../../aspose.words.fields/fieldstart/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
