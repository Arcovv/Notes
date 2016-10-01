# 🔧iOS Font Study

### 環境： 
(iOS 9.0), (Swift 2.2), (Xcode 7.3.1 Playground) 

Example font:
```swift
let font = UIFont.systemFontOfSize(20) 
```

## UIFont 基本屬性：

**familyName(String):**

字族 

ex: SF UI Display 

**fontName(String):**

字體名稱 

ex: SFUIDisplay-Regular 

**pointSize(CGFloat):**

from wiki: [wiki/點_(印刷)](https://zh.wikipedia.org/wiki/點_(印刷)) 

点（英语：point，pt），也音译磅因、磅，或因表示字级大小译为级，是印刷上所使用的一种磅数（长度）单位，用于表示字型的大小。72点相当于1英寸（1 point = 127⁄360 mm = 352.7 µm），12点称为1派卡。大小为12点的字可称为“12级字”。 
ex: 20.0 

**ascender(CGFloat):** 

![ascender](https://upload.wikimedia.org/wikipedia/commons/e/e3/Typographic_ascenders.png)

from wiki: [wiki/升部](https://zh.wikipedia.org/wiki/升部) 

在西文字体排印学中，升部（英语：Ascender）是指一个字体的字母中向上超过主线笔画的部分，也就是比x字高还要高的部分，是字体设计中一个重要的组成部分。 
升部，和降部笔画可以增强单词的识别率。因此，英国的高速公路标识放弃采用一律大写字母的做法，增强可读性。 
ex: 19.04... 

**descender(CGFloat):**

![descender](https://upload.wikimedia.org/wikipedia/commons/f/f6/Typographic_descenders.png)

from wiki: [wiki/降部](https://zh.wikipedia.org/wiki/降部) 

在西文字体排印學中，降部（英语：Descender）指的是一个字体中，字母向下延伸超过基线的笔画部分，也稱爲下延部。 
如右圖所示，字母y第二笔的“尾巴”部分就是降部。另外字母 v两条对角线连接的时候也有超过基线的部分，虽然很少，但也是降部。 
在多数字体中，降部主要指小写字母（如g、p和y）的延伸笔画部分。单在另一些字体中，降部也用于数字字符（特别是3、4、5、7和9），在排列的时候他们的主线高度和降部字母对齐，显得偏下。这些数字被称为旧式数字。（一些斜体字体，如「Computer Modern italic」，仅把字符4作为降部处理，而其他数字却没有，因此这种字体基本上不当做旧式字体。）一些字体的大写字母的尾巴也作为降部处理，如J和Q。 
与降部相对，字体中向上超过x字高的部分称为升部。 

ex: -4.82... 

**capHeight(CGFloat):**

![capHeight](https://upload.wikimedia.org/wikipedia/commons/thumb/3/39/Typography_Line_Terms.svg/361px-Typography_Line_Terms.svg.png)

from wiki: [wiki/大寫高度](https://zh.wikipedia.org/wiki/大寫高度) 

在西文字体排印学中，大写字高（英语：Cap height）是指某种字体中，位于基线（baseline）以上的大写字母的高度。尤其指相对平顺的字母“H”和“I”的高度。因为圆型的字母“O”和尖形字母“A”等，在设计中为保持视觉观感，其高度会有上下浮动（Overshoot）。而小写字母字高，指的就是X字高。 

ex: 14.09... 

**xHeight(CGFloat):**

![xHeight](https://upload.wikimedia.org/wikipedia/commons/thumb/3/39/Typography_Line_Terms.svg/361px-Typography_Line_Terms.svg.png)

from wiki: [wiki/X字高](https://zh.wikipedia.org/wiki/X字高) 

在西文字体排印学中，x字高，（英语：x-height或corpus size）是指字母的基本高度，精确地说，就是基线（英语：baseline）和主线之间的距离。特别的，它指称一个字体中小写字母x的高度（这也是这个词的语源），而实际上这也和字母a、c、e、m、n、o、r、s、u、v、w和z的高度是一样的。尽管如此，在现代字体设计领域里，x字高代表了一个字体的设计因素，因此在一些场合，字母x本身并不完全等于x字高。 
在西文中，除了上文提到的字母以外，其他小写字母的字高都要比x字高要大，并分为两类，一种是含有降部的字母，字母的笔画向下超过了基线，比如字母y、g、q和p；另一类是含有升部的字母，字母笔画含有向上部分，如l、k、b和d。x字高和字母主字高（英语：body height）的比例是考察一个字体设计的重要因素。 
在西文的具体字体以及排版术语中，x字高通常被称为一个ex，这和把大写字母M的宽度称为一个em的习惯类似 

ex: 10.52... 

**lineHeight(CGFloat):**

約等於 abs(font.descender) + abs(font.ascender) 

ex: 23.86... 

**leading(CGFloat):** 

![leading](https://github.com/YueJun1991/Notes/blob/master/images/font-study/lineHeight-wiki.png)

from wiki: [wiki/行距](https://zh.wikipedia.org/wiki/行距) 

在字體排印學，行距（Leading）指代字體連續行的基線間的距離。這個詞起源於手工排版的年代，鉛字之間通過插入鉛塊來增加垂直距離。這個術語仍然被應用於如 QuarkXPress、Adobe InDesign 等現代化的版面設計軟件。 
在以消費者爲導向的文字排版軟件中，這個概念通常指的是“line spacing”或“interline spacing”。 

from jianshu: [iOS 行距全攻略](http://www.jianshu.com/p/50b3d434cbc0 ) 

![leading-jianshu](https://github.com/YueJun1991/Notes/blob/master/images/font-study/lineHeight-jianshu.png)

在 iOS 方面，需要調整 NSMutableParagraphStyle 中的 lineSpacing 才能進行設定。 

ex: 0 
