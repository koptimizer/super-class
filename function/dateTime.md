### 현재 날짜 및 시간을 원하는 String으로 표현
```
myDateTime = datetime.datetime.now().strptime("%Y-%m-%d %H:%M:%S")
```

### String으로 된 날짜 및 시간을 datetime.datetime으로 변경
```
DateTimeStr = '2015-04-15 12:23:38'
myDateTime = datetime.datetime.strptime(DateTimeStr, '%Y-%m-%d %H:%M:%S')
```
