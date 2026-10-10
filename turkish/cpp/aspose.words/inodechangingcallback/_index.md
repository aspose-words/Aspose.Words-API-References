---
title: "Aspose::Words::INodeChangingCallback arayüzü"
linktitle: "INodeChangingCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::INodeChangingCallback arayüzü. Belge içinde düğümler eklendiğinde veya kaldırıldığında bildirim almak istiyorsanız bu arayüzü C++'ta uygulayın."
type: docs
weight: 79000
url: /tr/cpp/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface


Düğümler belgeye eklendiğinde veya kaldırıldığında bildirim almak istiyorsanız bu arayüzü uygulayın.

```cpp
class INodeChangingCallback : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [NodeInserted](./nodeinserted/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Bu belgeye ait bir düğüm başka bir düğüme eklendiğinde çağrılır. |
| virtual [NodeInserting](./nodeinserting/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Bu belgeye ait bir düğüm başka bir düğüme eklenmek üzereyken hemen önce çağrılır. |
| virtual [NodeRemoved](./noderemoved/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Bu belgeye ait bir düğüm ebeveyninden kaldırıldığında çağrılır. |
| virtual [NodeRemoving](./noderemoving/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Bu belgeye ait bir düğüm belgeden kaldırılmak üzereyken hemen önce çağrılır. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
