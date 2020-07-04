# youtube-clone
#### Html + CSS + JS 로 만든 youtube clone 코딩

# 
Link to 
[Demo](https://ceylon85.github.io/youtube-clone)  

# 
### 레이아웃 구성
`[Header, Video, Information, Upnext]`
# 
### 마크업 작성   
`Editor`: vs code   
`Icons`: Fontawesome   
`Fonts`: google Fonts
# 
### 1. Header
`.logo+.icons`
#### 1) Logo 
#### 2) Title
`.logo>(i+span.title)`
#### 3)icons [search, menu]
# 
### 2. Video
1) Video
비디오 태그 사용
- controls 속성을 사용하면 기본 비디오 구성이 나온다.
- Video 폴더를 만들어 가져온다.
# 
## 3. Information   
#### 1) Metadata    
`.metadata+.titleAndButton+.views`
- HashTag    
`ul.hashtag>li*3`
- Title box [Title / button]   
`span.title+button`   
- Views   
`.views>span.views`

#### 2) Action button     
`ul>(li>button)*5`   
Button 태그 안에 `<i>` 태그를 icons에 맞춰서 알맞게 넣는다. 
- like [like info] 
- unlike [unlike info]
- share
- save
- report

#### 3) channel info   
`.metadata+.info+.subscribe`
- metadata [img]

- info [ channel title. subscribers ]
`span.name+span.subscribers`

- subscriber button
`button.subscribe`
# 
### 4. Up next  
`span.title+ul>(li.item>img+(.info>(span.title+span.name+span.views))+button.moreBtn)*3`

- Video(img로 대체)
- info
- moreBtn

### CSS styling
- 변수정의 [color / size / font-size ]
```CSS
:root {
    /* Color */
    --white-color:#FFFFFF;
    --black-color: #140a00;
    --blue-color: #045fd4;
    --red-color: #ff0000;
    --grey-dark-color: #909090;
    --grey-light-color: #e0e0e0;

    /* Size */
    --padding: 16px;
    --avatar-size: 36px;

    /* Font Size */
    --font-large: 18px;
    --font-medium: 14px;
    --font-small: 12px;
    --font-micro: 10px;
}
```

#### media query 를 사용
- 평소에는 `flex-direction`이 `column` 이었다가 
일정 크기 이상이 되면 `row`로 변경 
```CSS
@media screen and (min-width: 768px){
    .infoAndUpNext{
        flex-direction: row;
        margin: var(--padding);
    }
}
```

