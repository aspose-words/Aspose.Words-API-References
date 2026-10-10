---
title: SignOptions.comments property
linktitle: comments property
articleTitle: comments property
second_title: Aspose.Words for Python
description: "SignOptions.comments property. Specifies comments on the digital signature"
type: docs
weight: 40
url: /zh/python-net/aspose.words.digitalsignatures/signoptions/comments/
---

## SignOptions.comments property

Specifies comments on the digital signature.
Default value is **empty string**().



```python
@property
def comments(self) -> str:
    ...

@comments.setter
def comments(self, value: str):
    ...

```

### Examples

Shows how to digitally sign documents.

```python
# 从 PKCS#12 存储创建 X.509 证书，该证书应包含私钥。
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# 创建将在我们的新数字签名中使用的注释和日期。
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'My comment'
sign_options.sign_time = datetime.datetime.now()
# 通过文件流从本地文件系统获取未签名的文档，
# 然后根据输出文件流的文件名创建其已签名副本。
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'DigitalSignatureUtil.SignDocument.docx', system_helper.io.FileMode.OPEN_OR_CREATE) as stream_out:
        aw.digitalsignatures.DigitalSignatureUtil.sign(src_stream=stream_in, dst_stream=stream_out, cert_holder=certificate_holder, sign_options=sign_options)
```

### See Also

* module [aspose.words.digitalsignatures](../../)
* class [SignOptions](../)

