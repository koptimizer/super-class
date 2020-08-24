### GET 기본 틀
```
 url = '기본 URL'
        info = 'URL에 추가해줄 정보'
        url += url+info

        html = requests.get(url)
        soup = BeautifulSoup(html.content, 'html.parser', from_encoding="utf-8")
 ```
 
 ### POST 기본 틀
 ```
  url = '기본 URL'
        info = 'URL에 추가해줄 정보'
        url += url+info

        # 웹서버에 POST로 보내기위한 POST Form
        postForm ={}

        html = requests.post(url, postForm)
        soup = BeautifulSoup(html.content, 'html.parser', from_encoding="utf-8")
 ```
 
 ### Table을 뽑아내서 pandas.Dataframe형태로 만들기
 ```
 table = soup.find("table", {"class" : "찾고자 하는 table의 class명"})
        table_html = str(table)
        table_df_list = pd.read_html(table_html)[0]
 ```
