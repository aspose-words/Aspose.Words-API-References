---
title: CertificateHolder.Create
linktitle: Create
articleTitle: Create
second_title: 用于 .NET 的 Aspose.Words
description: CertificateHolder Create 方法. 使用 PKCS12 存储的字节数组及其密码创建 CertificateHolder 对象 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(*byte[], SecureString*) {#create}

使用 PKCS12 存储的字节数组及其密码创建 CertificateHolder 对象。

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| certBytes | Byte[] | 包含来自 X.509 证书的数据的字节数组。 |
| password | SecureString | 访问 X.509 证书数据所需的密码。 |

### 返回值

CertificateHolder 的一个实例

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| InvalidParameterException | 抛出如果**证书字节**一片空白 |
| InvalidParameterException | 抛出如果**密码**一片空白 |
| SecurityException | 如果 PKCS12 存储不包含别名则抛出 |
| IOException | 如果密码错误或文件损坏，则抛出。 |

## 例子

展示如何创建 CertificateHolder 对象。

```csharp
// 下面是四种创建 CertificateHolder 对象的方法。
// 1 - 将 PKCS #12 文件加载到字节数组中并应用其密码：
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - 将 PKCS #12 文件加载到字节数组中，并应用安全密码：
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// 如果证书有对应别名的私钥，
// 我们可以使用别名来获取它们各自的键。首先，我们将检查有效的别名。
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

// 3 - 使用有效的别名：
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - 传递“null”作为别名，以便使用返回私钥的第一个可用别名：
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### 也可以看看

* class [CertificateHolder](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)

---

## Create(*byte[], string*) {#create_1}

使用 PKCS12 存储的字节数组及其密码创建 CertificateHolder 对象。

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| certBytes | Byte[] | 包含来自 X.509 证书的数据的字节数组。 |
| password | String | 访问 X.509 证书数据所需的密码。 |

### 返回值

CertificateHolder 的一个实例

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| InvalidParameterException | 抛出如果**证书字节**一片空白 |
| InvalidParameterException | 抛出如果**密码**一片空白 |
| SecurityException | 如果 PKCS12 存储不包含别名则抛出 |
| IOException | 如果密码错误或文件损坏，则抛出。 |

## 例子

展示如何创建 CertificateHolder 对象。

```csharp
// 下面是四种创建 CertificateHolder 对象的方法。
// 1 - 将 PKCS #12 文件加载到字节数组中并应用其密码：
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - 将 PKCS #12 文件加载到字节数组中，并应用安全密码：
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// 如果证书有对应别名的私钥，
// 我们可以使用别名来获取它们各自的键。首先，我们将检查有效的别名。
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

// 3 - 使用有效的别名：
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - 传递“null”作为别名，以便使用返回私钥的第一个可用别名：
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### 也可以看看

* class [CertificateHolder](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)

---

## Create(*string, string*) {#create_2}

使用 PKCS12 存储的路径及其密码创建 CertificateHolder 对象。

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 证书文件的名称。 |
| password | String | 访问 X.509 证书数据所需的密码。 |

### 返回值

CertificateHolder 的一个实例

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| InvalidParameterException | 抛出如果**文件名**一片空白 |
| InvalidParameterException | 抛出如果**密码**一片空白 |
| SecurityException | 如果 PKCS12 存储不包含别名则抛出 |
| IOException | 如果密码错误或文件损坏，则抛出。 |

## 例子

展示如何对文档进行数字签名。

```csharp
// 从 PKCS#12 存储创建 X.509 证书，其中应包含私钥。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// 创建一个评论和日期，它将与我们的新数字签名一起应用。
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// 通过文件流从本地文件系统中获取未签名的文档，
// 然后创建一个由输出文件流的文件名确定的签名副本。
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### 也可以看看

* class [CertificateHolder](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)

---

## Create(*string, string, string*) {#create_3}

使用 PKCS12 存储的路径、其密码和别名创建 CertificateHolder 对象，使用该对象可以找到私钥和证书。

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 证书文件的名称。 |
| password | String | 访问 X.509 证书数据所需的密码。 |
| alias | String | 证书及其私钥的关联别名 |

### 返回值

CertificateHolder 的一个实例

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| InvalidParameterException | 抛出如果**文件名**一片空白 |
| InvalidParameterException | 抛出如果**密码**一片空白 |
| SecurityException | 如果 PKCS12 存储不包含别名则抛出 |
| IOException | 如果密码错误或文件损坏，则抛出。 |
| SecurityException | 如果没有具有给定别名的私钥，则抛出 |

## 例子

展示如何创建 CertificateHolder 对象。

```csharp
// 下面是四种创建 CertificateHolder 对象的方法。
// 1 - 将 PKCS #12 文件加载到字节数组中并应用其密码：
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - 将 PKCS #12 文件加载到字节数组中，并应用安全密码：
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// 如果证书有对应别名的私钥，
// 我们可以使用别名来获取它们各自的键。首先，我们将检查有效的别名。
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

// 3 - 使用有效的别名：
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - 传递“null”作为别名，以便使用返回私钥的第一个可用别名：
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### 也可以看看

* class [CertificateHolder](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)
