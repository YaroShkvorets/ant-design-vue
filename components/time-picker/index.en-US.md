---
category: Components
type: Data Entry
title: TimePicker
cover: https://gw.alipayobjects.com/zos/alicdn/h04Zsl98I/TimePicker.svg
---

To select/input a time.

## When To Use

By clicking the input box, you can select a time from a popup panel.

## API

| Property | Description | Type | Default | Version |
| --- | --- | --- | --- | --- |
| allowClear | Whether allow clearing text | boolean | true |  |
| autofocus | If get focus when component mounted | boolean | false |  |
| bordered | Whether has border style | boolean | true |  |
| clearIcon | The custom clear icon | v-slot:clearIcon | - |  |
| clearText | The clear tooltip of icon | string | clear |  |
| disabled | Determine whether the TimePicker is disabled | boolean | false |  |
| disabledHours | To specify the hours that cannot be selected | function() | - |  |
| disabledMinutes | To specify the minutes that cannot be selected | function(selectedHour) | - |  |
| disabledSeconds | To specify the seconds that cannot be selected | function(selectedHour, selectedMinute) | - |  |
| format | To set the time format | string | `HH:mm:ss` |  |
| getPopupContainer | To set the container of the floating layer, while the default is to create a div element in body | function(trigger) | - |  |
| hideDisabledOptions | Whether hide the options that can not be selected | boolean | false |  |
| hourStep | Interval between hours in picker | number | 1 |  |
| inputReadOnly | Set the `readonly` attribute of the input tag (avoids virtual keyboard on touch devices) | boolean | false |  |
| minuteStep | Interval between minutes in picker | number | 1 |  |
| open(v-model) | Whether to popup panel | boolean | false |  |
| placeholder | Display when there's no value | string \| \[string, string] | `Select a time` |  |
| popupClassName | The className of panel | string | - |  |
| popupStyle | The style of panel | CSSProperties | - |  |
| renderExtraFooter | Called from time picker panel to render some addon to its bottom | v-slot:renderExtraFooter | - |  |
| secondStep | Interval between seconds in picker | number | 1 |  |
| showNow | Whether to show `Now` button on panel | boolean | - |  |
| suffixIcon | The custom suffix icon | v-slot:suffixIcon | - |  |
| use12Hours | Display as 12 hours format, with default format `h:mm:ss a` | boolean | false |  |
| value(v-model) | To set time | [dayjs](https://day.js.org/) | - |  |
| valueFormat | optional, format of binding value. If not specified, the binding value will be a Date object | string，[date formats](https://day.js.org/docs/en/display/format) | - |  |

### events

| Events Name | Description | Arguments |
| --- | --- | --- |
| change | a callback function, can be executed when the selected time is changing | function(time: dayjs \| string, timeString: string): void |
| openChange | a callback function which will be called while panel opening/closing | (open: boolean): void |

## Methods

| Name    | Description  |
| ------- | ------------ |
| blur()  | remove focus |
| focus() | get focus    |

### TimeRangePicker

Same props from [RangePicker](/components/date-picker/#RangePicker) of DatePicker. And includes additional props:

| Property | Description | Type | Default | Version |
| --- | --- | --- | --- | --- |
| order | Order start and end time | boolean | true |  |

## FAQ
### How to use DatePicker with customize date library（like moment.js \| dayjs \| date-fns）？

Please refer [replace date](/docs/vue/replace-date)