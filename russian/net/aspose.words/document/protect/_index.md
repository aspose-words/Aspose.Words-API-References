---
title: Document.Protect
linktitle: Protect
articleTitle: Protect
second_title: Aspose.Words для .NET
description: Защитите свои документы без усилий с Document Protect. Предотвратите несанкционированные изменения, сохранив свой существующий пароль нетронутым или используя случайный.
type: docs
weight: 690
url: /ru/net/aspose.words/document/protect/
---
## Protect(*[ProtectionType](../../protectiontype/)*) {#protect}

Защищает документ от изменений без изменения существующего пароля или назначает случайный пароль.

```csharp
public void Protect(ProtectionType type)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| type | ProtectionType | Указывает тип защиты документа. |

## Примечания

Если документ защищен, пользователь может вносить только ограниченные изменения, например, добавлять аннотации, вносить исправления или заполнять формы.

Если вы защищаете документ, а у документа уже есть пароль защиты, , то существующий пароль защиты не изменяется.

Если вы защищаете документ, а у документа нет пароля защиты, этот метод назначает случайный пароль, который делает невозможным снятие защиты документа в Microsoft Word, но вы все равно можете снять защиту документа в Aspose.Words, так как он не требует ввода пароля при снятии защиты.

## Примеры

Показывает, как отключить защиту раздела.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Применить защиту от записи к каждому разделу документа.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// Отключаем защиту от записи для первого раздела.
doc.Sections[0].ProtectedForForms = false;

// В этом выходном документе мы сможем свободно редактировать первый раздел,
// и мы сможем редактировать только содержимое поля формы во втором разделе.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Смотрите также

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Protect(*[ProtectionType](../../protectiontype/), string*) {#protect_1}

Защищает документ от изменений и при необходимости устанавливает пароль защиты.

```csharp
public void Protect(ProtectionType type, string password)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| type | ProtectionType | Указывает тип защиты документа. |
| password | String | Пароль для защиты документа с помощью . Укажите`нулевой` или пустую строку, если вы хотите защитить документ без пароля. |

## Примечания

Если документ защищен, пользователь может вносить только ограниченные изменения, например, добавлять аннотации, вносить исправления или заполнять формы.

Обратите внимание, что защита документа отличается от защиты от записи. Защита от записи указывается с помощью[`WriteProtection`](../writeprotection/).

## Примеры

Показывает, как защитить и снять защиту документа.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Если мы откроем этот документ в Microsoft Word, намереваясь его редактировать,
// нам нужно будет применить пароль, чтобы обойти защиту.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Обратите внимание, что защита распространяется только на пользователей Microsoft Word, открывающих наш документ.
// Мы никак не зашифровали документ, и нам не нужен пароль для его программного открытия и редактирования.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// Существует два способа снятия защиты с документа.
// 1 - Без пароля:
doc.Unprotect();

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

doc.Unprotect("WrongPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 2 - С правильным паролем:
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### Смотрите также

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
