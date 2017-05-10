# CSS만 사용하여 tooltip 만드는 방법

## Step 1) HTML 추가하기

```html
<div class="tooltip">Hover over me
  <span class="tooltiptext">Tooltip text</span>
</div>
```
## Step 2) CSS 추가하기

```css
/* Tooltip container */
.tooltip {
    position: relative;
    display: inline-block;
    border-bottom: 1px dotted black; /* If you want dots under the hoverable text */
}

/* Tooltip text */
.tooltip .tooltiptext {
    visibility: hidden;
    width: 120px;
    background-color: #555;
    color: #fff;
    text-align: center;
    padding: 5px 0;
    border-radius: 6px;

    /* Position the tooltip text */
    position: absolute;
    z-index: 1;
    bottom: 125%;
    left: 50%;
    margin-left: -60px;

    /* Fade in tooltip */
    opacity: 0;
    transition: opacity 1s;
}

/* Tooltip arrow */
.tooltip .tooltiptext::after {
    content: "";
    position: absolute;
    top: 100%;
    left: 50%;
    margin-left: -5px;
    border-width: 5px;
    border-style: solid;
    border-color: #555 transparent transparent transparent;
}

/* Show the tooltip text when you mouse over the tooltip container */
.tooltip:hover .tooltiptext {
    visibility: visible;
    opacity: 1;
}
```


## Refer
[이 공부는 여기를 보고 그대로 따라함](https://www.w3schools.com/howto/howto_css_tooltip.asp)
[위 예제에 대한 툴팁의 더 자세한 설명](https://www.w3schools.com/css/css_tooltip.asp)
[클릭할 수 있는 툴팁 만드는 법](https://www.w3schools.com/howto/howto_js_popup.asp)