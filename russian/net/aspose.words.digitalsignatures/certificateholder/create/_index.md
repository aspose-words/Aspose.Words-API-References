---
title: Create
second_title: Справочник по API Aspose.Words для .NET
description: Создает объект CertificateHolder используя массив байтов хранилища PKCS12 и его пароль.
type: docs
weight: 10
url: /ru/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(byte[], SecureString) {#create}

Создает объект CertificateHolder, используя массив байтов хранилища PKCS12 и его пароль.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| certBytes | Byte[] | Массив байтов, содержащий данные из сертификата X.509. |
| password | SecureString | Пароль, необходимый для доступа к данным сертификата X.509. |

### Возвращаемое значение

Экземпляр CertificateHolder

### Исключения

| исключение | условие |
| --- | --- |
| InvalidParameterException | Брошен, если **certBytes** нулевой |
| InvalidParameterException | Брошен, если **пароль** нулевой |
| SecurityException | Брошен, если хранилище PKCS12 не содержит псевдонимов |
| IOException | Брошен, если есть неправильный пароль или поврежденный файл. |

### Примеры

Показывает, как создавать объекты CertificateHolder.

```csharp
// Ниже приведены четыре способа создания объектов CertificateHolder.
// 1 - Загрузить файл PKCS #12 в массив байтов и применить его пароль:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Загрузите файл PKCS #12 в массив байтов и примените безопасный пароль:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Если в сертификате есть закрытые ключи, соответствующие псевдонимам,
// мы можем использовать псевдонимы для получения соответствующих ключей. Во-первых, мы проверим действительные псевдонимы.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12Store(certStream, "aw".ToCharArray());
    IEnumerator enumerator = pkcs12Store.Aliases.GetEnumerator();

    while (enumerator.MoveNext())
    {
        if (enumerator.Current != null)
        {
            string currentAlias = enumerator.Current.ToString();
            if (pkcs12Store.IsKeyEntry(currentAlias) && pkcs12Store.GetKey(currentAlias).Key.IsPrivate)
            {
                Console.WriteLine($"Valid alias found: {enumerator.Current}");
            }
        }
    }
}

// 3 - Используйте допустимый псевдоним:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Передайте "null" в качестве псевдонима, чтобы использовать первый доступный псевдоним, который возвращает закрытый ключ:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Смотрите также

* class [CertificateHolder](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../certificateholder/)
* сборка [Aspose.Words](../../../)

---

## Create(byte[], string) {#create_1}

Создает объект CertificateHolder, используя массив байтов хранилища PKCS12 и его пароль.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| certBytes | Byte[] | Массив байтов, содержащий данные из сертификата X.509. |
| password | String | Пароль, необходимый для доступа к данным сертификата X.509. |

### Возвращаемое значение

Экземпляр CertificateHolder

### Исключения

| исключение | условие |
| --- | --- |
| InvalidParameterException | Брошен, если **certBytes** нулевой |
| InvalidParameterException | Брошен, если **пароль** нулевой |
| SecurityException | Брошен, если хранилище PKCS12 не содержит псевдонимов |
| IOException | Брошен, если есть неправильный пароль или поврежденный файл. |

### Примеры

Показывает, как создавать объекты CertificateHolder.

```csharp
// Ниже приведены четыре способа создания объектов CertificateHolder.
// 1 - Загрузить файл PKCS #12 в массив байтов и применить его пароль:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Загрузите файл PKCS #12 в массив байтов и примените безопасный пароль:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Если в сертификате есть закрытые ключи, соответствующие псевдонимам,
// мы можем использовать псевдонимы для получения соответствующих ключей. Во-первых, мы проверим действительные псевдонимы.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12Store(certStream, "aw".ToCharArray());
    IEnumerator enumerator = pkcs12Store.Aliases.GetEnumerator();

    while (enumerator.MoveNext())
    {
        if (enumerator.Current != null)
        {
            string currentAlias = enumerator.Current.ToString();
            if (pkcs12Store.IsKeyEntry(currentAlias) && pkcs12Store.GetKey(currentAlias).Key.IsPrivate)
            {
                Console.WriteLine($"Valid alias found: {enumerator.Current}");
            }
        }
    }
}

// 3 - Используйте допустимый псевдоним:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Передайте "null" в качестве псевдонима, чтобы использовать первый доступный псевдоним, который возвращает закрытый ключ:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Смотрите также

* class [CertificateHolder](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../certificateholder/)
* сборка [Aspose.Words](../../../)

---

## Create(string, string) {#create_2}

Создает объект CertificateHolder, используя путь к хранилищу PKCS12 и его пароль.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла сертификата. |
| password | String | Пароль, необходимый для доступа к данным сертификата X.509. |

### Возвращаемое значение

Экземпляр CertificateHolder

### Исключения

| исключение | условие |
| --- | --- |
| InvalidParameterException | Брошен, если **имя файла** нулевой |
| InvalidParameterException | Брошен, если **пароль** нулевой |
| SecurityException | Брошен, если хранилище PKCS12 не содержит псевдонимов |
| IOException | Брошен, если есть неправильный пароль или поврежденный файл. |

### Примеры

Показывает, как подписывать документы цифровой подписью.

```csharp
// Создайте сертификат X.509 из хранилища PKCS#12, который должен содержать закрытый ключ.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Создайте комментарий и дату, которые будут применяться с нашей новой цифровой подписью.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Берём неподписанный документ из локальной файловой системы через файловый поток,
// затем создайте его подписанную копию, определяемую именем файла выходного файлового потока.
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
* пространство имен [Aspose.Words.DigitalSignatures](../../certificateholder/)
* сборка [Aspose.Words](../../../)

---

## Create(string, string, string) {#create_3}

Создает объект CertificateHolder, используя путь к хранилищу PKCS12, его пароль и псевдоним, с помощью которого будут найдены закрытый ключ и сертификат.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла сертификата. |
| password | String | Пароль, необходимый для доступа к данным сертификата X.509. |
| alias | String | Связанный псевдоним для сертификата и его закрытый ключ |

### Возвращаемое значение

Экземпляр CertificateHolder

### Исключения

| исключение | условие |
| --- | --- |
| InvalidParameterException | Брошен, если **имя файла** нулевой |
| InvalidParameterException | Брошен, если **пароль** нулевой |
| SecurityException | Брошен, если хранилище PKCS12 не содержит псевдонимов |
| IOException | Брошен, если есть неправильный пароль или поврежденный файл. |
| SecurityException | Брошен, если нет закрытого ключа с данным псевдонимом |

### Примеры

Показывает, как создавать объекты CertificateHolder.

```csharp
// Ниже приведены четыре способа создания объектов CertificateHolder.
// 1 - Загрузить файл PKCS #12 в массив байтов и применить его пароль:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Загрузите файл PKCS #12 в массив байтов и примените безопасный пароль:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Если в сертификате есть закрытые ключи, соответствующие псевдонимам,
// мы можем использовать псевдонимы для получения соответствующих ключей. Во-первых, мы проверим действительные псевдонимы.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12Store(certStream, "aw".ToCharArray());
    IEnumerator enumerator = pkcs12Store.Aliases.GetEnumerator();

    while (enumerator.MoveNext())
    {
        if (enumerator.Current != null)
        {
            string currentAlias = enumerator.Current.ToString();
            if (pkcs12Store.IsKeyEntry(currentAlias) && pkcs12Store.GetKey(currentAlias).Key.IsPrivate)
            {
                Console.WriteLine($"Valid alias found: {enumerator.Current}");
            }
        }
    }
}

// 3 - Используйте допустимый псевдоним:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Передайте "null" в качестве псевдонима, чтобы использовать первый доступный псевдоним, который возвращает закрытый ключ:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Смотрите также

* class [CertificateHolder](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../certificateholder/)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
