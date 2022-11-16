---
title: INodeChangingCallback
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, если хотите получать уведомления о вставке или удалении узлов в документе.
type: docs
weight: 652
url: /ru/java/com.aspose.words/inodechangingcallback/
---
```
public interface INodeChangingCallback
```

Реализуйте этот интерфейс, если хотите получать уведомления о вставке или удалении узлов в документе.
## Методы

| Метод | Описание |
| --- | --- |
| [nodeInserted(NodeChangingArgs args)](#nodeInserted-com.aspose.words.NodeChangingArgs-) | Вызывается, когда узел, принадлежащий этому документу, был вставлен в другой узел. |
| [nodeInserting(NodeChangingArgs args)](#nodeInserting-com.aspose.words.NodeChangingArgs-) | Вызывается непосредственно перед вставкой узла, принадлежащего этому документу, в другой узел. |
| [nodeRemoved(NodeChangingArgs args)](#nodeRemoved-com.aspose.words.NodeChangingArgs-) | Вызывается, когда узел, принадлежащий этому документу, был удален из своего родителя. |
| [nodeRemoving(NodeChangingArgs args)](#nodeRemoving-com.aspose.words.NodeChangingArgs-) | Вызывается непосредственно перед удалением из документа узла, принадлежащего этому документу. |
### nodeInserted(NodeChangingArgs args) {#nodeInserted-com.aspose.words.NodeChangingArgs-}
```
public abstract void nodeInserted(NodeChangingArgs args)
```


Вызывается, когда узел, принадлежащий этому документу, был вставлен в другой узел.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs) |  |

### nodeInserting(NodeChangingArgs args) {#nodeInserting-com.aspose.words.NodeChangingArgs-}
```
public abstract void nodeInserting(NodeChangingArgs args)
```


Вызывается непосредственно перед вставкой узла, принадлежащего этому документу, в другой узел.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs) |  |

### nodeRemoved(NodeChangingArgs args) {#nodeRemoved-com.aspose.words.NodeChangingArgs-}
```
public abstract void nodeRemoved(NodeChangingArgs args)
```


Вызывается, когда узел, принадлежащий этому документу, был удален из своего родителя.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs) |  |

### nodeRemoving(NodeChangingArgs args) {#nodeRemoving-com.aspose.words.NodeChangingArgs-}
```
public abstract void nodeRemoving(NodeChangingArgs args)
```


Вызывается непосредственно перед удалением из документа узла, принадлежащего этому документу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs) |  |
