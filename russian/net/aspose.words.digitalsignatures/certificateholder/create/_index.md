---
title: CertificateHolder.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words для .NET
description: Легко создайте объект CertificateHolder из массива байтов PKCS12 и пароля. Упростите управление сертификатами с помощью нашего интуитивного метода.
type: docs
weight: 10
url: /ru/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(*byte[], SecureString*) {#create}

Создает[`CertificateHolder`](../) объект, использующий байтовый массив хранилища PKCS12 и его пароль.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| certBytes | Byte[] | Массив байтов, содержащий данные из сертификата X.509. |
| password | SecureString | Пароль, необходимый для доступа к данным сертификата X.509. |

### Возвращаемое значение

Пример[`CertificateHolder`](../)

### Исключения

| исключение | условие |
| --- | --- |
| InvalidParameterException | Выброшено, если*certBytes* является`нулевой` |
| InvalidParameterException | Выброшено, если*password* является`нулевой` |
| SecurityException | Вызывается, если хранилище PKCS12 не содержит псевдонимов. |
| IOException | Вызывается, если введен неверный пароль или файл поврежден. |

## Примеры

Показывает, как создавать объекты CertificateHolder.

```csharp
// Ниже приведены четыре способа создания объектов CertificateHolder.
// 1 — Загрузить файл PKCS #12 в массив байтов и применить его пароль:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 — Загрузить файл PKCS #12 в массив байтов и применить безопасный пароль:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Если сертификат имеет закрытые ключи, соответствующие псевдонимам,
// мы можем использовать псевдонимы для извлечения соответствующих им ключей. Сначала мы проверим допустимые псевдонимы.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    foreach (string currentAlias in pkcs12Store.Aliases)
    {
        if ((currentAlias != null) &&
            (pkcs12Store.IsKeyEntry(currentAlias) &&
             pkcs12Store.GetKey(currentAlias).Key.IsPrivate))
        {
            Console.WriteLine($"Valid alias found: {currentAlias}");
        }
    }
}

// 3 - Используйте допустимый псевдоним:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Передайте «null» в качестве псевдонима, чтобы использовать первый доступный псевдоним, который возвращает закрытый ключ:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Смотрите также

* class [CertificateHolder](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)

---

## Create(*byte[], string*) {#create_1}

Создает[`CertificateHolder`](../) объект, использующий байтовый массив хранилища PKCS12 и его пароль.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| certBytes | Byte[] | Массив байтов, содержащий данные из сертификата X.509. |
| password | String | Пароль, необходимый для доступа к данным сертификата X.509. |

### Возвращаемое значение

Пример[`CertificateHolder`](../)

### Исключения

| исключение | условие |
| --- | --- |
| InvalidParameterException | Выброшено, если*certBytes* является`нулевой` |
| InvalidParameterException | Выброшено, если*password* является`нулевой` |
| SecurityException | Вызывается, если хранилище PKCS12 не содержит псевдонимов. |
| IOException | Вызывается, если введен неверный пароль или файл поврежден. |

## Примеры

Показывает, как создавать объекты CertificateHolder.

```csharp
// Ниже приведены четыре способа создания объектов CertificateHolder.
// 1 — Загрузить файл PKCS #12 в массив байтов и применить его пароль:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 — Загрузить файл PKCS #12 в массив байтов и применить безопасный пароль:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Если сертификат имеет закрытые ключи, соответствующие псевдонимам,
// мы можем использовать псевдонимы для извлечения соответствующих им ключей. Сначала мы проверим допустимые псевдонимы.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    foreach (string currentAlias in pkcs12Store.Aliases)
    {
        if ((currentAlias != null) &&
            (pkcs12Store.IsKeyEntry(currentAlias) &&
             pkcs12Store.GetKey(currentAlias).Key.IsPrivate))
        {
            Console.WriteLine($"Valid alias found: {currentAlias}");
        }
    }
}

// 3 - Используйте допустимый псевдоним:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Передайте «null» в качестве псевдонима, чтобы использовать первый доступный псевдоним, который возвращает закрытый ключ:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Смотрите также

* class [CertificateHolder](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)

---

## Create(*string, string*) {#create_2}

Создает[`CertificateHolder`](../)объект, использующий путь к хранилищу PKCS12 и его пароль.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла сертификата. |
| password | String | Пароль, необходимый для доступа к данным сертификата X.509. |

### Возвращаемое значение

Пример[`CertificateHolder`](../)

### Исключения

| исключение | условие |
| --- | --- |
| InvalidParameterException | Выброшено, если*fileName* является`нулевой` |
| InvalidParameterException | Выброшено, если*password* является`нулевой` |
| SecurityException | Вызывается, если хранилище PKCS12 не содержит псевдонимов. |
| IOException | Вызывается, если введен неверный пароль или файл поврежден. |

## Примеры

Показывает, как подписывать документы цифровой подписью.

```csharp
// Создайте сертификат X.509 из хранилища PKCS#12, который должен содержать закрытый ключ.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Создайте комментарий и дату, которые будут применены к нашей новой цифровой подписи.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Берем неподписанный документ из локальной файловой системы через файловый поток,
// затем создаем его подписанную копию, определяемую именем файла выходного потока.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Смотрите также

* class [CertificateHolder](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)

---

## Create(*string, string, string*) {#create_3}

Создает[`CertificateHolder`](../) объект, использующий путь к хранилищу PKCS12, его пароль и псевдоним, с помощью которого будут найдены закрытый ключ и сертификат.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла сертификата. |
| password | String | Пароль, необходимый для доступа к данным сертификата X.509. |
| alias | String | Связанный псевдоним для сертификата и его закрытый ключ |

### Возвращаемое значение

Пример[`CertificateHolder`](../)

### Исключения

| исключение | условие |
| --- | --- |
| InvalidParameterException | Выброшено, если*fileName* является`нулевой` |
| InvalidParameterException | Выброшено, если*password* является`нулевой` |
| SecurityException | Вызывается, если хранилище PKCS12 не содержит псевдонимов. |
| IOException | Вызывается, если введен неверный пароль или файл поврежден. |
| SecurityException | Вызывается, если нет закрытого ключа с указанным псевдонимом |

## Примеры

Показывает, как создавать объекты CertificateHolder.

```csharp
// Ниже приведены четыре способа создания объектов CertificateHolder.
// 1 — Загрузить файл PKCS #12 в массив байтов и применить его пароль:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 — Загрузить файл PKCS #12 в массив байтов и применить безопасный пароль:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Если сертификат имеет закрытые ключи, соответствующие псевдонимам,
// мы можем использовать псевдонимы для извлечения соответствующих им ключей. Сначала мы проверим допустимые псевдонимы.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    foreach (string currentAlias in pkcs12Store.Aliases)
    {
        if ((currentAlias != null) &&
            (pkcs12Store.IsKeyEntry(currentAlias) &&
             pkcs12Store.GetKey(currentAlias).Key.IsPrivate))
        {
            Console.WriteLine($"Valid alias found: {currentAlias}");
        }
    }
}

// 3 - Используйте допустимый псевдоним:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Передайте «null» в качестве псевдонима, чтобы использовать первый доступный псевдоним, который возвращает закрытый ключ:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Смотрите также

* class [CertificateHolder](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)
