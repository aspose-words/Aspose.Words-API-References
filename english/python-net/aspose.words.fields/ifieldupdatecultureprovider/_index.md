---
title: IFieldUpdateCultureProvider class
linktitle: IFieldUpdateCultureProvider class
articleTitle: IFieldUpdateCultureProvider class
second_title: Aspose.Words for Python
description: "aspose.words.fields.IFieldUpdateCultureProvider class. When implemented, provides a System.Globalization.CultureInfo object that should be used during the update of a particular field."
type: docs
weight: 1250
url: /python-net/aspose.words.fields/ifieldupdatecultureprovider/
---

## IFieldUpdateCultureProvider class

When implemented, provides a System.Globalization.CultureInfo object that should be used during the update of a particular field.



### Examples

Shows how to specify a culture which parses date/time formatting for each field (FieldUpdateCultureProvider).

```python
class FieldUpdateCultureProvider(aw.fields.IFieldUpdateCultureProvider):

    def get_culture(self, name, field):

        def set_custom_culture(name):
            switch_condition = name
            if switch_condition == 'ru-RU':
                culture = aw.CultureInfo(name, False)
                format = culture.datetime_format
                format.month_names = ['месяц 1', 'месяц 2', 'месяц 3', 'месяц 4', 'месяц 5', 'месяц 6', 'месяц 7', 'месяц 8', 'месяц 9', 'месяц 10', 'месяц 11', 'месяц 12', '']
                format.month_genitive_names = format.month_names
                format.abbreviated_month_names = ['мес 1', 'мес 2', 'мес 3', 'мес 4', 'мес 5', 'мес 6', 'мес 7', 'мес 8', 'мес 9', 'мес 10', 'мес 11', 'мес 12', '']
                format.abbreviated_month_genitive_names = format.abbreviated_month_names
                format.day_names = ['день недели 7', 'день недели 1', 'день недели 2', 'день недели 3', 'день недели 4', 'день недели 5', 'день недели 6']
                format.abbreviated_day_names = ['день 7', 'день 1', 'день 2', 'день 3', 'день 4', 'день 5', 'день 6']
                format.shortest_day_names = ['д7', 'д1', 'д2', 'д3', 'д4', 'д5', 'д6']
                format.am_designator = 'До полудня'
                format.pm_designator = 'После полудня'
                pattern = 'yyyy MM (MMMM) dd (dddd) hh:mm:ss tt'
                format.long_date_pattern = pattern
                format.long_time_pattern = pattern
                format.short_date_pattern = pattern
                format.short_time_pattern = pattern
                return culture
            elif switch_condition == 'en-US':
                return aw.CultureInfo(name, False)
            else:
                return None
```

### See Also

* module [aspose.words.fields](../)

