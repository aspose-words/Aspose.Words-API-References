---
title: CertificateHolder.Create
second_title: Справочник по API Aspose.Words для .NET
description: CertificateHolder метод. СоздаетCertificateHolder объект использующий массив байтов хранилища PKCS12 и его пароль.
type: docs
weight: 10
url: /ru/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(byte[], SecureString) {#create}

Создает[`CertificateHolder`](../) объект, использующий массив байтов хранилища PKCS12 и его пароль.

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
| InvalidParameterException | Выбрасывается, если*certBytes* является`нулевой` |
| InvalidParameterException | Выбрасывается, если*password* является`нулевой` |
| SecurityException | Выдается, если хранилище PKCS12 не содержит псевдонимов. |
| IOException | Выдается, если указан неверный пароль или поврежден файл. |

### Примеры

Показывает, как создавать объекты CertificateHolder.

```csharp
// Ниже приведены четыре способа создания объектов CertificateHolder.
// 1 — загрузить файл PKCS #12 в массив байтов и применить к нему пароль:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 — Загрузите файл PKCS #12 в массив байтов и примените безопасный пароль:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Если сертификат имеет закрытые ключи, соответствующие псевдонимам,
// мы можем использовать псевдонимы для получения соответствующих ключей. Сначала мы проверим допустимые псевдонимы.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
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

// 3 – Используйте действительный псевдоним:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 — передать «null» в качестве псевдонима, чтобы использовать первый доступный псевдоним, возвращающий закрытый ключ:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Смотрите также

* class [CertificateHolder](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../certificateholder/)
* сборка [Aspose.Words](../../../)

---

## Create(byte[], string) {#create_1}

Создает[`CertificateHolder`](../) объект, использующий массив байтов хранилища PKCS12 и его пароль.

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
| InvalidParameterException | Выбрасывается, если*certBytes* является`нулевой` |
| InvalidParameterException | Выбрасывается, если*password* является`нулевой` |
| SecurityException | Выдается, если хранилище PKCS12 не содержит псевдонимов. |
| IOException | Выдается, если указан неверный пароль или поврежден файл. |

### Примеры

Показывает, как создавать объекты CertificateHolder.

```csharp
// Ниже приведены четыре способа создания объектов CertificateHolder.
// 1 — загрузить файл PKCS #12 в массив байтов и применить к нему пароль:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 — Загрузите файл PKCS #12 в массив байтов и примените безопасный пароль:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Если сертификат имеет закрытые ключи, соответствующие псевдонимам,
// мы можем использовать псевдонимы для получения соответствующих ключей. Сначала мы проверим допустимые псевдонимы.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
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

// 3 – Используйте действительный псевдоним:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 — передать «null» в качестве псевдонима, чтобы использовать первый доступный псевдоним, возвращающий закрытый ключ:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Смотрите также

* class [CertificateHolder](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../certificateholder/)
* сборка [Aspose.Words](../../../)

---

## Create(string, string) {#create_2}

Создает[`CertificateHolder`](../) объект, используя путь к хранилищу PKCS12 и его пароль.

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
| InvalidParameterException | Выбрасывается, если*fileName* является`нулевой` |
| InvalidParameterException | Выбрасывается, если*password* является`нулевой` |
| SecurityException | Выдается, если хранилище PKCS12 не содержит псевдонимов. |
| IOException | Выдается, если указан неверный пароль или поврежден файл. |

### Примеры

Показывает, как подписывать документы цифровой подписью.

```csharp
// Создайте сертификат X.509 из хранилища PKCS#12, который должен содержать закрытый ключ.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Создаем комментарий и дату, которые будут применяться с нашей новой цифровой подписью.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Берем неподписанный документ из локальной файловой системы через файловый поток,
// затем создаем его подписанную копию, определенную именем файла потока выходного файла.
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

Создает[`CertificateHolder`](../) объект, используя путь к хранилищу PKCS12, его пароль и псевдоним, по которому будут найдены закрытый ключ и сертификат.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла сертификата. |
| password | String | Пароль, необходимый для доступа к данным сертификата X.509. |
| alias | String | Связанный псевдоним сертификата и его закрытый ключ. |

### Возвращаемое значение

Пример[`CertificateHolder`](../)

### Исключения

| исключение | условие |
| --- | --- |
| InvalidParameterException | Выбрасывается, если*fileName* является`нулевой` |
| InvalidParameterException | Выбрасывается, если*password* является`нулевой` |
| SecurityException | Выдается, если хранилище PKCS12 не содержит псевдонимов. |
| IOException | Выдается, если указан неверный пароль или поврежден файл. |
| SecurityException | Вызывается, если нет закрытого ключа с данным псевдонимом. |

### Примеры

Показывает, как создавать объекты CertificateHolder.

```csharp
// Ниже приведены четыре способа создания объектов CertificateHolder.
// 1 — загрузить файл PKCS #12 в массив байтов и применить к нему пароль:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 — Загрузите файл PKCS #12 в массив байтов и примените безопасный пароль:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Если сертификат имеет закрытые ключи, соответствующие псевдонимам,
// мы можем использовать псевдонимы для получения соответствующих ключей. Сначала мы проверим допустимые псевдонимы.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
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

// 3 – Используйте действительный псевдоним:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 — передать «null» в качестве псевдонима, чтобы использовать первый доступный псевдоним, возвращающий закрытый ключ:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Смотрите также

* class [CertificateHolder](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../certificateholder/)
* сборка [Aspose.Words](../../../)


