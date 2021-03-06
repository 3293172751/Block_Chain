[toc]



ð¶âð«ï¸goè¯­è¨å®æ¹ç¼ç¨æåï¼[https://pkg.go.dev/std](https://pkg.go.dev/std)

>   goè¯­è¨çå®æ¹ææ¡£å­¦ä¹ ç¬è®°å¾å¨ï¼æ¨èå»å®ç½å­¦ä¹ 

ð¶âð«ï¸æçå­¦ä¹ ç¬è®°ï¼github: [https://github.com/3293172751/golang-rearn](https://github.com/3293172751/golang-rearn)

---

**åºåé¾ææ¯ï¼ä¹ç§°ä¹ä¸ºåå¸å¼è´¦æ¬ææ¯ï¼**ï¼æ¯ä¸ç§äºèç½æ°æ®åºææ¯ï¼å¶ç¹ç¹æ¯å»ä¸­å¿åï¼å¬å¼éæï¼è®©æ¯ä¸ä¸ªäººåå¯åä¸çæ°æ®åºè®°å½

>   â¤ï¸ððå³äºåºåé¾ææ¯ï¼å¯ä»¥å³æ³¨æï¼å±åå­¦ä¹ æ´å¤çåºåé¾ææ¯ãåå®¢[http://nsddd.top](http://nsddd.top)

---

# 45å¤©å­¦ä¼go --ç¬¬å­å¤© ï¼goè¯­è¨ççå½æ°ãæ°ç»



## å½æ°

### å¿åå½æ°

>   è¡¥åç¬¬äºå¤©å¯¹å½æ°ç»å°¾

**å¿åå½æ°ææçæï¼å°±æ¯æ²¡æåå­çå½æ°ï¼å¦ææä»¬å¸ææä¸ªå½æ°åªä½¿ç¨ä¸æ¬¡ï¼é£ä¹å¯ä»¥ä½¿ç¨å¿åå½æ°ï¼ä½ä¹å¯ä»¥å¤æ¬¡ä½¿ç¨**



#### ä¸æ¬¡æ§å¿åå½æ°

**å¨å®ä¹å¿åå½æ°çæ¶åå°±è°ç¨ï¼æ­¤æ¶å¿åå½æ°å°±åªè½ä½¿ç¨ä¸æ¬¡**

```go
fun main(){
	//å®ä¹å³è°ç¨
    func(n1 int,n2 int)int{
        return n1 + n2
    }(10,20)
	//æ­¤æ¶å¨å®ä¹çæ¶ååæ¶è°ç¨
}
```

```
30
```



#### ç»åéè°ç¨

**è¿ç§æ¹å¼çå¿åå½æ°å¯ä»¥å¤æ¬¡è°ç¨ï¼ä¹åæä»¬è¯´è¿å½æ°ä¹æ¯ä¸ç§æ°æ®ç±»åï¼é£ä¹å°è¿ä¸ªå½æ°ç´æ¥å®ä¹ä¸ä¸ªåéç¶åèµå¼**

```go
fun main(){
	//å®ä¹å³è°ç¨
    a := func(n1 int,n2 int)int{
        return n1 - n2
    }
	//æ­¤æ¶å¨å®ä¹çæ¶ååæ¶è°ç¨
    res := a(30,20)
    fmt.Println("res="res)
    res2 := a(30,40)
    fmt.Println("res3=",res3)
}
```

```
res= 10
res3= -10
```



### å¨å±å¿åå½æ°

```go
var(
	Fun1 = func(n1 int,n2 int)int{
		return n1 * n2
		}
	)          //å®ä¹å¨å±å¿åå½æ°'F'è¦å¤§å

//è°ç¨
func main(){
    a := Fun1(10,100)
    fmt.Println("a=",a)
}
```

```
a=1000
```

---

### å¿åæ»ç»å®æ
```
package main

import (
	"fmt"
)
//å¨å±å¿åå½æ°
var(
  t = func(a int, b int) int {
    return a + b 
  }
)
var t3 = func(a int, b int) int {
    return a * b 
  }(123,123)

func main() {
	fmt.Println("Hello, World!")
  a := 1
  b := (^a+1)  //åå
  fmt.Println(b)
  fmt.Println("*t = ",t) //è¿ä¸ªå°æ¹æ¯å®çå°å
  fmt.Println("func t = ",t(10,26))
  fmt.Println("func t3= ",t3)
  
  //å¶ä»å¿åå½æ°
    //ä¸æ¬¡æ§å¿å
  t2 := func(a int, b int) int {
    return a + b 
  }(12,312)
  fmt.Println("func t2 = ",t2)

  func(a int, b int) int {
    return a * b 
  }(12,312)
  
  //å¤æ¬¡ä½¿ç¨çå¿å
  t5:= func(a int, b int) int {
  return a + b 
  }
  fmt.Println("func t5 = ",t5(234,123421))
}

```
![image](https://user-images.githubusercontent.com/86140903/180969213-9114bcec-2786-4481-a5ad-82ec73436f2c.png)


## é­å

**é­åå°±æ¯ä¸ä¸ª==å½æ°ä¸ç¸å³çå¼ç¨ç¯å¢==ç»æçä¸ä¸ª<u>æ´ä½ï¼å®ä½</u>ï¼**

Go è¯­è¨æ¯æå¿åå½æ°ï¼å¯ä½ä¸ºé­åãå¿åå½æ°æ¯ä¸ä¸ª"åè"è¯­å¥æè¡¨è¾¾å¼ãå¿åå½æ°çä¼è¶æ§å¨äºå¯ä»¥ç´æ¥ä½¿ç¨å½æ°åçåéï¼ä¸å¿ç³æã

>   ä»¥ä¸å®ä¾ä¸­ï¼æä»¬åå»ºäºå½æ° getSequence() ï¼è¿åå¦å¤ä¸ä¸ªå½æ°ãè¯¥å½æ°çç®çæ¯å¨é­åä¸­éå¢ i åéï¼ä»£ç å¦ä¸ï¼

#### å®ä¾

```go
package main

import "fmt"

func getSequence() func() int {
    i:=0               //func()æ¯ä¸ä¸ªå¿åå½æ°
    //getSequence()æ¯ä¸ä¸ªå½æ°ï¼è¿åçæ°æ®ç±»åæ¯func()int
   return func() int {
      i+=1 
     return i  
   }
}

func main(){
   /* nextNumber ä¸ºä¸ä¸ªå½æ°ï¼å½æ° i ä¸º 0 */
   nextNumber := getSequence()  //å°å½æ°ç»åéNex,ç¸å½äºå¿åå½æ°

   /* è°ç¨ nextNumber å½æ°ï¼i åéèªå¢ 1 å¹¶è¿å */
   fmt.Println(nextNumber())
   fmt.Println(nextNumber())
   fmt.Println(nextNumber())

   /* åå»ºæ°çå½æ° nextNumber1ï¼å¹¶æ¥çç»æ */
   nextNumber1 := getSequence()  
   fmt.Println(nextNumber1())
   fmt.Println(nextNumber1())
}
```

**ä»¥ä¸ä»£ç æ§è¡ç»æä¸ºï¼**

```
1
2
3
1
2
```

#### é­åçè¯´æ

```
	i:=0               //func()æ¯ä¸ä¸ªå¿åå½æ°
    //getSequence()æ¯ä¸ä¸ªå½æ°ï¼è¿åçæ°æ®ç±»åæ¯func()int
return func() int {
     i+=1 
     return i  
 }
```

**==è¿åçæ¯ä¸ä¸ªå¿åå½æ°ï¼==åæ¶è¿ä¸ªå¿åå½æ°å¼ç¨å°å½æ°å¤çiï¼å æ­¤è¿ä¸ªå¿åå½æ°åiå½¢æä¸ä¸ªæ´ä½ï¼ææ é­å**

>   å¯ä»¥è¿æ ·çè§£ï¼é­åæ¯ä¸ä¸ªç±»classï¼èiæ¯å­æ®µï¼å½æ°æ¯ä¸ä¸ªæä½ï¼èå½æ°åè¿ä¸ªiææé­å

**å½æä»¬åå¤çè°ç¨få½æ°ï¼å ä¸ºiåªæ¯åå§åä¸æ¬¡ï¼å æ­¤æ¯è°ç¨æ­¤ä¸æ¬¡å°±ç´¯å ä¸æ¬¡**

**å³é®ï¼å°±æ¯è¿åçå½æ°å¼ç¨å°åªäºåéï¼å½æ°ä¸åªäºåéææé­å**

#### æ¡ä¾

![image-20220109141602331](https://s2.loli.net/2022/01/09/4lTbFmDxeBMI8E9.png)





## å½æ°defer

**å¨å½æ°ä¸­ï¼éå¸¸éç¨åå»ºèµæºï¼æ¯å¦ï¼æ°æ®åºè¿æ¥ï¼æä»¶ç­ï¼ï¼ä¸ºäºå¨å½æ°æ§è¡å®æ¯åï¼å³ä½¿çéæ¾èµæºï¼Goæä¾äºdeferï¼å»¶æ¶æºå¶ï¼**   --- `æ `

```go
package main
import "fmt"

func sum(n1 int, n2 int) int{
	defer fmt.Println("ok1 n1=",n1)
	defer fmt.Println("ok1 n2=",n2)
	res := n1 + n2 
	fmt.Println("ok1 res=",res)
	return res
}

func main(){
	res := sum(10,20)
	fmt.Println("res=",res)
}
```

![image-20220109143800029](https://s2.loli.net/2022/01/09/Zc8X5HmzShWeNMp.png)

**æ³¨æï¼**

1.   å½æ§è¡å°deferæ¶åï¼ç³»ç»ä¼å°deferè¯­å¥åå¥å°ä¸ä¸ªç¬ç«çæ ä¸­ï¼deferæ ï¼ï¼ææ¶ä¸æ§è¡
2.   å½å½æ°æ§è¡å®æ¯ååä»deferä¸­æç§**åå¥ååº**çæ¹å¼åºæ ï¼ç¶åæ§è¡
3.   å½æ°ä¸­çres æåæ§è¡ï¼è¾åº30
4.   æåæ§è¡mainä¸­çè¯­å¥
5.   å¨deferè¯­å¥å¥æ çæ¶åï¼ä¹ä¼å°ç¸å³çå¼åæ¶æ¾å¥å°æ 

>   æå¤§æ¦è®¤ä¸ºå°±è·C++ä¸­çæé å½æ° åææå½æ°`~`ç±»ä¼¼

**å³deferä½ç¨æ¯å¨å½æ°æ§è¡å®æ¯åï¼å¯ä»¥åæ¶çéæ¾å½æ°åå»ºçèµæº**

```go
//æä»¶æä½
defer file Close()

//æ°æ®åºæä½
defer connect.close()       //connectæ¯æ°æ®åºçæ¸¸æ 
```



## å­ç¬¦ä¸²å¸¸ç¨çç³»ç»å½æ°

```go
package utils
import (
	"fmt"
	"strconv"
	"strings"
)

var str string = "å­¦golangä½¿æå¿«ä¹ï¼"

// å³äºstringçå¸¸ç¨å½æ°

// 1. len(str) åå»ºå½æ°ï¼è¿åå­ç¬¦ä¸²é¿åº¦ï¼æå­èï¼1ä¸ªæ±å­3å­èï¼1å­æ¯1å­è
//è¿ä¸ªå½æ°æ¯åå»ºå½æ°ï¼åprintfä¸æ ·ï¼  //åªéè¦`fmt`å
func F1(){
    fmt.Println(len(str))
}

// 2. range []rune(str)  å­ç¬¦ä¸²éåï¼å¤çä¸­æé®é¢ è½¬æruneåç
func F2() {
	for _,value := range []rune(str) {
		fmt.Printf("%c \n",value)
	}
}

// 3. stringè½¬æ´æ° strconv.Atoi(str) è¿ä¸ªå½æ°æ¯ strconv.ParseInt(s string, base int, bitSize int) (i int64 err error)çç®åç
func F3() {
	num, _ := strconv.Atoi("666")
	fmt.Printf("num type is %T,value is %v", num, num) 
    // num type is int,value is 666

}

// 4. æ´æ°è½¬string strconv.Itoa(666) æ¯strconv.FormatInt(i int64, base int) stringçç®åç

// 5. string to []byte  b := []byte(str)
func F5(){
	 b := []byte(str)
	 fmt.Printf("%T %v\n", b, b) // type of b is []uint8
}

// 6. []byte to string   s := string([]byte{77,88,99})
func F6(){
	 s := string([]byte{77,88,99})
	 fmt.Printf("%T %v\n", s, s) // string MXc
}

// 7. åè¿å¶æ°è½¬2 8 16è¿å¶å­ç¬¦ä¸²  strconv.FormatInt(i int64, base int) string  base->2,8,16

// 8. å¤æ­å­ç¬¦ä¸²sæ¯å¦åå«å­ä¸²substr strings.Contains(s, substr string) bool

// 9. ç»è®¡å­ä¸²åºç°æ¬¡æ° strings.Count(s, sep string) int
func F9() {
	s := "A man who helps you when you are in trouble and who leaves you when you are successful is a real friend."

	fmt.Println(strings.Count(s,"you")) // 4

	s = "lv"
	fmt.Println(strings.Count(s,"")) // 3

}

// 10. å¤æ­è¿ä¸ªå­ç¬¦ä¸²æ¯å¦ç¸ç­ str1 == str2 åºåå¤§å°åï¼ ä¸åºåå¤§å°åæ¹å¼strings.EqualFold(s, t string) bool

// 11. å­ä¸²sepå¨å­ç¬¦ä¸²sä¸­ç¬¬ä¸æ¬¡/æåä¸æ¬¡åºç°çä½ç½®ï¼ä¸å­å¨åè¿å-1  Index(s, sep string) int/LastIndex(s, sep string) int

// 12. å°nä¸ªoldå­ä¸²æ¿æ¢ä¸ºnewå­ç¬¦ä¸²ï¼n<0ä¼æ¿æ¢ææoldå­ä¸² strings.Replace(s, old, new string, n int) string

// 13. å¤§å°åè½¬æ¢ strings.ToUpper  /ToLower

// 14. æsepæåå­ç¬¦ä¸²ï¼è¿åä¸ä¸ªslice  strings.Split(s, sep string) []string

// 15. å°å­ç¬¦ä¸²sliceä»¥sepä¸ºåéç¬¦ç»åæä¸ä¸ªå­ç¬¦ä¸² strings.Join(a []string, sep string) string

// 16. Trimç³»å Trim(s string, cutset string) string å»é¤å·¦å³ä¸¤è¾¹æå®å­ç¬¦ä¸²  TrimRight/TrimLeft
// 	TrimSpace(s string) string å»é¤å·¦å³ä¸¤è¾¹ç©ºç½
//  TrimPrefix(s, prefix string) string /TrimSuffix(s, suffix string) string å»é¤å/åç¼

// 17. å¤æ­sæ¯å¦æåç¼/åç¼å­ç¬¦ä¸²prefix   HasPrefix(s, prefix string) bool  / HasSuffix
func main(){
    
}
```



## æ¥æåæ¶é´ç¸å³å½æ°

1.   æ¶é´åæ¥æç¸å³çå½æ°éè¦å¯¼å¥timeå[https://pkg.go.dev/time@go1.17.6](https://pkg.go.dev/time@go1.17.6)

2.   time.Time ç±»åï¼ç¨äºè¡¨ç¤ºæ¶é´

     ```go
     package main
     import(
     	"fmt"
     	"time"
     )
     func main(){
         now := time.Time()
         fmt.Printf("now=%v now type=%T",now,now)
     
         fmt.Println(now.Year())      //è·åå°å¹´
         fmt.Println(int(now.Month()))      //è·åå°æ
         fmt.Println(now.Day())      //è·åå°æ¥
         fmt.Println(now.Hour())      //è·åå°æ¶
         fmt.Println(now.Minute())      //è·åå°å
         fmt.Println(now.Second())      //è·åå°ç§
     }
     ```

     ![image-20220109151948003](https://s2.loli.net/2022/01/09/SebIThU4GB3xXCH.png)

     

     

     #### æ¶é´å¸¸é

     **å¸¸éå°±æ¯å¨ç¨åºä¸­å¯ç¨äºè·åæå®æ¶é´åä½çæ¶é´**

     ```go
     const (
     	Nanosecond  Duration = 1
     	Microsecond          = 1000 * Nanosecond
     	Millisecond          = 1000 * Microsecond
     	Second               = 1000 * Millisecond
     	Minute               = 60 * Second
     	Hour                 = 60 * Minute
     )
     ```

     >   æ¯å¦æ³æ¿å°100æ¯«ç§

     ```
     100 * time.Millisecond
     ```

     **å¦ææä»¬æ³è¦ä¼ç ä¸æ®µæ¶é´ï¼å¿é¡»è¦ä½¿ç¨å°æ¶é´å¸¸é**

â	

#### ç»åsleepæ¥ä½¿ç¨æ¶é´å¸¸é

>   éæ±ï¼æ¯éä¸ç§éæå°ä¸ä¸ªæ°å­ï¼æå°å°10æ¶å°±éåº
>
>   æ¯é0.1ç§æå°ä¸ä¸ªæ°å­ï¼æå°5ç§éåº**ï¼ä¸å¯ä»¥ä½¿ç¨time.Second * 0.1,ç¼è¯ä¸è½éè¿ï¼åªè½ç¨millisecond(æ¯«ç§) * 100)**

```go
package main
import (
    "fmt"
    "time"
)

func main(){
i := 0
j := 0
 for{
     i++
     fmt.Println(i)  //æå°
     time.Sleep(time.Second)   //ä¼ç ï¼æ¯ç§éæ§è¡ä¸æ¬¡
     if i == 10{
         break
     }
 }
    for{
        j++
        fmt.Println(j)
        time.Sleep(time.Millisecond * 100)
        if i == 20{
            break
        }
    }
}
```

![image-20220109154141855](https://s2.loli.net/2022/01/09/kQdxJsaft5wM4nB.png)



### unixæ¶é´æ³åunixnanoæ¶é´æ³

**ä½ç¨æ¯ï¼è·åéæºæ°å­**

>   **unix :è·åç§æ°éæº**
>
>   **unixnano:è·åçº³ç§éå³æ°**

```
now = time.Now()
fmt.Printf("unixæ¶é´æ³ä¸º=%v \n unixnanoæ¶é´æ=%v",now.unix(),now.unixnano())
```

![image-20220109160542484](https://s2.loli.net/2022/01/09/nwSfaEKBhON96gD.png)

#### func (Time) [Unix](https://cs.opensource.google/go/go/+/go1.17.6:src/time/time.go;l=1134) [Â¶](https://pkg.go.dev/time@go1.17.6#Time.Unix)

```
func (t Time) Unix() int64
```

Unix returns t as a Unix time, the number of seconds elapsed since January 1, 1970 UTC. The result does not depend on the location associated with t. Unix-like operating systems often record time as a 32-bit count of seconds, but since the method here returns a 64-bit value it is valid for billions of years into the past or future.

```go
package main

import (
	"fmt"
	"time"
)

func main() {
	// 1 billion seconds of Unix, three ways.
	fmt.Println(time.Unix(1e9, 0).UTC())     // 1e9 seconds
	fmt.Println(time.Unix(0, 1e18).UTC())    // 1e18 nanoseconds
	fmt.Println(time.Unix(2e9, -1e18).UTC()) // 2e9 seconds - 1e18 nanoseconds

    t := time.Date(2001, time.September, 9, 1, 46, 40, 0, time.UTC)
    fmt.Println(t.Unix())     // seconds since 1970
    fmt.Println(t.UnixNano()) // nanoseconds since 1970
}
```



#### func (Time) [UnixMicro](https://cs.opensource.google/go/go/+/go1.17.6:src/time/time.go;l=1152) [Â¶](https://pkg.go.dev/time@go1.17.6#Time.UnixMicro)added in go1.17

```
func (t Time) UnixMicro() int64
```

UnixMicro returns t as a Unix time, the number of microseconds elapsed since January 1, 1970 UTC. The result is undefined if the Unix time in microseconds cannot be represented by an int64 (a date before year -290307 or after year 294246). The result does not depend on the location associated with t.

#### func (Time) [UnixMilli](https://cs.opensource.google/go/go/+/go1.17.6:src/time/time.go;l=1143) [Â¶](https://pkg.go.dev/time@go1.17.6#Time.UnixMilli)added in go1.17

```
func (t Time) UnixMilli() int64
```

UnixMilli returns t as a Unix time, the number of milliseconds elapsed since January 1, 1970 UTC. The result is undefined if the Unix time in milliseconds cannot be represented by an int64 (a date more than 292 million years before or after 1970). The result does not depend on the location associated with t.

#### func (Time) [UnixNano](https://cs.opensource.google/go/go/+/go1.17.6:src/time/time.go;l=1162) [Â¶](https://pkg.go.dev/time@go1.17.6#Time.UnixNano)

```
func (t Time) UnixNano() int64
```

UnixNano returns t as a Unix time, the number of nanoseconds elapsed since January 1, 1970 UTC. The result is undefined if the Unix time in nanoseconds cannot be represented by an int64 (a date before the year 1678 or after 2262). Note that this means the result of calling UnixNano on the zero Time is undefined. The result does not depend on the location associated with t.



#### ç»è®¡ä»£ç æ§è¡æ¶é´

>   ç¼åä¸ä¸ªä»£ç æ¥ç»è®¡å½æ°testæ§è¡çæ¶é´

```go
package main

import (
	"fmt"
	"time"
    "strconv"         //ç¨æ¥è½¬æ¢
)
func test(){
    str := ""
    for i :=0;i < 10000; i++{
        str += "hello" + strconv.Itoa(i)
        fmt.Println(str)
    }
}
func main() {
    start := time.Now().Unix()
    test()
    end := time.Now().unix()
    fmt.Println("æ§è¡testæ¶èçæ¶é´ä¸º(s)ï¼",end - start)
}    
```

![image-20220109162120408](https://s2.loli.net/2022/01/09/l8TLEcMs4fNzIKx.png)



## Golangåç½®å½æ°

Golangå°åï¼[https://pkg.go.dev/builtin@go1.17.6](https://pkg.go.dev/builtin@go1.17.6)

#### func [new](https://cs.opensource.google/go/go/+/go1.17.6:src/builtin/builtin.go;l=194) [Â¶](https://pkg.go.dev/builtin@go1.17.6#new)

```
func new(Type) *Type
```

The new built-in function allocates memory. The first argument is a type, not a value, and the value returned is a pointer to a newly allocated zero value of that type.

>   **new ä¸»è¦ç¨æ¥åéåå­ï¼ä¸»è¦æ¯ç¨æ¥åéå¼ç±»å,æ¬èº«æ¯ä¸ä¸ªå°åï¼é»è®¤æ¯å­æ¾0è¿ä¸ªæ°æ®ç©ºé´çå°å,å°åæ¯ç±ç³»ç»åéç**

```go
package main
import "fmt"
func main(){
	num1 := 100
	fmt.Printf("num1çç±»åä¸º:%T,\n num1çå¼ä¸º:%v,\n num1çå°åä¸º:%v",num1,num1,&num1)
    
    num2 = new(int)
    fmt.Printf("num2çç±»åä¸º:%T,\n num2çå¼ä¸º:%v,\n num2çå°åä¸º:%v",num2,num2,&num2)  /*intç±»å   å¼ä¸ºæåç©ºé´çå°å    æ¬ççå°åä¸ºæéçå°å    */
}
```

![image-20220109163125076](https://s2.loli.net/2022/01/09/7pi1yuPCFAIsEwK.png)

![image-20220109164028360](https://s2.loli.net/2022/01/09/bvqIE1LtnZeJGrQ.png)

**æä¹å°num2çå¼ååºï¼ -- `*`åå°åçå¼**

```go
fmt.Printf("num2çå¼ä¸º:%v",*num2)    
```

```
num2çå¼ä¸ºï¼0   //ä¿®æ¹  *num2 = 100
```



## Golangéè¯¯å¤çæºå¶

**å¤çæ¹å¼ï¼defer,panic,recover**   --**è®©ç¨åºæ´å å¥å£®**

**Goä¸­å¯ä»¥æåºä¸ä¸ªpanicçå¼å¸¸ï¼ç¶åå¨deferä¸­éè¿==recoveræè·è¿ä¸ªå¼å¸¸==ï¼ç¶åæ­£å¸¸å¤ç**

ä½¿ç¨deferårecoveræ¥å¤çå¼å¸¸ã

#### func [panic](https://cs.opensource.google/go/go/+/go1.17.6:src/builtin/builtin.go;l=232) [Â¶](https://pkg.go.dev/builtin@go1.17.6#panic)

**panicåç½®å½æ°æ¥åä¸ä¸ªinterface{}ç±»åçå¼ä½ä¸ºåæ°,å¯ä»¥æ¥æ¶errorç±»ååéï¼è¾åºéè¯¯ä¿¡æ¯ï¼å¹¶éåºç¨åº**

```
func panic(v interface{})
```

**The panic built-in function stops normal execution of the current goroutine.** When a function F calls panic, normal execution of F stops immediately. Any functions whose execution was deferred by F are run in the usual way, and then F returns to its caller. To the caller G, the invocation of F then behaves like a call to panic, terminating G's execution and running any deferred functions. This continues until all functions in the executing goroutine have stopped, in reverse order. At that point, the program is terminated with a non-zero exit code. This termination sequence is called panicking and can be controlled by the built-in function recover.

```go
defer func(){
	/*å¿åå½æ°*/ 
	err := recover()   //åç½®å½æ°ï¼å¯ä»¥æè·å°å¼å¸¸
    if err != ni{//è¯´ææè·å°å¼å¸¸
        fmt.Println("err=",err) 
        fmt.Println("åéé®ä»¶ç»admin@qq,com")
    }         //è¿éå¯ä»¥å°éè¯¯åéç»ç®¡çå
}()     //å¿åå½æ°çè°ç¨
num := 10/0           //éè¯¯ä»£ç 
```

### èªå®ä¹éè¯¯

```
errors.New("éè¯¯ç±»å")    //è¿åä¸ä¸ªerrorç±»åçå¼ï¼è¡¨ç¤ºä¸ä¸ªéè¯¯
```

>   å½æ°è¯»åinit.configä¿¡æ¯ï¼å¦ææä»¶åä¼ å¥ä¸æ­£ç¡®ï¼è¿åä¸ä¸ªèªå®ä¹éè¯¯

```go
package main
import (
	"fmt"
    "errors"
)
func readConf(name string) (err error){
	if name = "config.ini"{
	//"è¯»å"
	return nil
	}else{
	//è¿åä¸ä¸ªèªå®ä¹éè¯¯
	return errors.New("è¯»åæä»¶éè¯¯")
	}
}

func test02(){
    err := readConf("config.ini")
    if err != nil{
        //å¦æåçéè¯¯ï¼å°±è¾åºéè¯¯å¹¶ä¸ç»æ­¢ç¨åºï¼æ­¤æ¶ä½¿ç¨panic
        panic(err)
    }
    //ä¸åçéè¯¯
    fmt.Println("test02()ç»§ç»­æ§è¡...")
}
func mian(){
    //æµè¯
    test02()
}
```



