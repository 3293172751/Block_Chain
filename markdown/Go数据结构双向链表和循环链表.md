ð¶âð«ï¸goè¯­è¨å®æ¹ç¼ç¨æåï¼[https://golang.org/](https://golang.org/)  

>   goè¯­è¨çå®æ¹ææ¡£å­¦ä¹ ç¬è®°å¾å¨ï¼æ¨èå»å®ç½å­¦ä¹ 

ð¶âð«ï¸æçå­¦ä¹ ç¬è®°ï¼github: [https://github.com/3293172751/golang-rearn](https://github.com/3293172751/golang-rearn)

---

**åºåé¾ææ¯ï¼ä¹ç§°ä¹ä¸ºåå¸å¼è´¦æ¬ææ¯ï¼**ï¼æ¯ä¸ç§äºèç½æ°æ®åºææ¯ï¼å¶ç¹ç¹æ¯å»ä¸­å¿åï¼å¬å¼éæï¼è®©æ¯ä¸ä¸ªäººåå¯åä¸çæ°æ®åºè®°å½

>   â¤ï¸ððå³äºåºåé¾ææ¯ï¼å¯ä»¥å³æ³¨æï¼å±åå­¦ä¹ æ´å¤çåºåé¾ææ¯ãåå®¢[http://nsddd.top](http://nsddd.top)

---



[toc]

# ð¶âð«ï¸goè¯­è¨å®æ¹ç¼ç¨æåï¼[https://golang.org/](https://golang.org/)  

>   goè¯­è¨çå®æ¹ææ¡£å­¦ä¹ ç¬è®°å¾å¨ï¼æ¨èå»å®ç½å­¦ä¹ 

ð¶âð«ï¸æçå­¦ä¹ ç¬è®°ï¼github: [https://github.com/3293172751/golang-rearn](https://github.com/3293172751/golang-rearn)

---

**åºåé¾ææ¯ï¼ä¹ç§°ä¹ä¸ºåå¸å¼è´¦æ¬ææ¯ï¼**ï¼æ¯ä¸ç§äºèç½æ°æ®åºææ¯ï¼å¶ç¹ç¹æ¯å»ä¸­å¿åï¼å¬å¼éæï¼è®©æ¯ä¸ä¸ªäººåå¯åä¸çæ°æ®åºè®°å½

>   â¤ï¸ððå³äºåºåé¾ææ¯ï¼å¯ä»¥å³æ³¨æï¼å±åå­¦ä¹ æ´å¤çåºåé¾ææ¯ãåå®¢[http://nsddd.top](http://nsddd.top)

---



[toc]

# Goè¯­è¨æ°æ®ç»æååé¾è¡¨åå¾ªç¯é¾è¡¨

> ååé¾è¡¨åªè½ä»å¤´ååæ¥è¯¢ï¼ä½æ¯ååé¾è¡¨æ¯å¯ä»¥ååçï¼æé«çæç

**ä»£ç  â å é¤**

```go
func DelHerNode(head *HeroNode, id int) {
	temp := head
	flag := false
	//æ¾å°è¦å é¤ç»ç¹çnoï¼åtempçä¸ä¸ä¸ªç»ç¹çnoæ¯è¾
	for {
		if temp.next == nil {//è¯´æå°é¾è¡¨çæå
			break
		} else if temp.next.no == id {
			//è¯´ææä»¬æ¾å°äº.
			flag = true
			break
		}
		temp = temp.next
	}
	if flag {//æ¾å°, å é¤
		temp.next = temp.next.next //ok
		if temp.next != nil {
			temp.next.pre = temp 
		}
	} else {
		fmt.Println("sorry, è¦å é¤çidä¸å­å¨")
	}
}
```



#### å¨ä»£ç 

```go
package main

import (
	"fmt"
)

//å®ä¹ä¸ä¸ªheronode
type HeroNode struct {
	no       int
	name     string
	nickname string

	pre  *HeroNode //è¡¨ç¤ºæååä¸ä¸ªç»ç¹
	next *HeroNode //è¡¨ç¤ºæåä¸ä¸ä¸ªèç¹
}

//ç»ååé¾è¡¨æå¥èç¹ -- ååé¾è¡¨
// é¡ºåºå¾éè¦ --
func InsertHerNode2(head *HeroNode, newHeroNode *HeroNode) {
	//æè·¯
	//1. æ¾å°éå½çèç¹ä½ç½®
	//2. åå»ºä¸ä¸ªè¾å©æ¥ç¹temp
	temp := head
	var flag bool
	for {
		//è®©æå¥ç»ç¹çnoåtempçä¸ä¸ä¸ªèç¹çnoè¿è¡æ¯è¾
		if temp.next == nil {
			//è¯´æææ«å°¾ï¼ç´æ¥æå¥å°å°¾é¨
			break
		} else if temp.next.no > newHeroNode.no {
			//æ¡ä»¶æç«ï¼è¯´æè¿ä¸ªnewHeroNodeæå¥å°tempåé¢
			break //è·³åºforå¾ªç¯  ç´æ¥æå¥
		} else if temp.next.no == newHeroNode.no {
			//ç¸ç­çè¯æä»¬æéä¸åè®¸æå¥è¿ä¸ªidï¼å ä¸ºå·²ç»æäº
			fmt.Println("æç¸åçèç¹ï¼é£ä¹ä¸å¯ä»¥æå¥")
			flag = true
			break
		}
		temp = temp.next

	}
	if flag {
		//è¡¨ç¤ºæ­¤æ¶è¿ä¸ªç¸ç­
		fmt.Println("å¯¹ä¸èµ·ï¼å·²ç»å­å¨", newHeroNode.no)
		return
	} else {
		newHeroNode.next = temp.next
		newHeroNode.pre = temp //ok
		//æ­¤æ¶åé¡¹ç»ç¹å®ç°äº
		//æ³¨æé¡ºåºå¾éè¦
		if temp.next != nil {
			temp.next.pre = newHeroNode //ok
		}

		temp.next = newHeroNode
	}

}

//æ¾ç¤ºé¾è¡¨
//ä»ç¶ä½¿ç¨åé¡¹é¾è¡¨æ¾ç¤ºæ¹å¼
func ListHeroNode(head *HeroNode) {
	//æ³¨æï¼ä¸å®è¦ç»å¤´ç»ç¹
	//åå¤æ­è¯¥é¾è¡¨æ¯å¦ä¸ºä¸ä¸ªç©ºé¾è¡¨
	temp := head
	if temp.next == nil {
		fmt.Println("ç©ºé¾è¡¨æ æ³æ¾ç¤º")
		return
	}
	//éå
	for {
		// if temp.next = nil{
		// 	break
		// }
		fmt.Println("èç¹ä¿¡æ¯å¦ä¸:"+"[",
			temp.next.no, temp.next.name, temp.next.nickname, "]===>")

		//å¤æ­æ¯å¦å°é¾è¡¨æå
		// if temp.next.next == nil{
		// 	break
		// }      !!!!æ¥éæ éå¾ªç¯
		temp = temp.next
		if temp.next == nil {
			break
		}
	}
}

//å°ååé¾è¡¨éåºæå°åºæ¥
func ListHeroNode2(head *HeroNode) {
	//æ³¨æï¼ä¸å®è¦ç»å¤´ç»ç¹
	//åå¤æ­è¯¥é¾è¡¨æ¯å¦ä¸ºä¸ä¸ªç©ºé¾è¡¨
	temp := head

	//å¤æ­ç©ºé¾è¡¨
	if temp.next == nil {
		fmt.Println("ç©ºé¾è¡¨æ æ³æ¾ç¤º")
		return
	}

	//è®©tempå®ä½å°ååé¾è¡¨çæåèç¹
	for {
		if temp.next == nil {
			break
		}
		temp = temp.next //å¦åæåä¸ä¸ä¸ªç»ç¹
	}

	//æ­¤æ¶å·²ç»æ¯æåç»ç¹äº
	//éå
	for {
		fmt.Println("ååé¾è¡¨ååæåºèç¹ä¿¡æ¯å¦ä¸:"+"[",
			temp.no, temp.name, temp.nickname, "]===>")

		//å¤æ­æ¯å¦å°äºè¡¨å¤´
		temp = temp.pre

		if temp.pre == nil {
			break
		}
	}
}
func DelHerNode(head *HeroNode, id int) {
	temp := head
	flag := false
	//æ¾å°è¦å é¤ç»ç¹çnoï¼åtempçä¸ä¸ä¸ªç»ç¹çnoæ¯è¾
	for {
		if temp.next == nil { //è¯´æå°é¾è¡¨çæå
			break
		} else if temp.next.no == id {
			//è¯´ææä»¬æ¾å°äº.
			flag = true
			break
		}
		temp = temp.next
	}
	if flag { //æ¾å°, å é¤
		temp.next = temp.next.next //ok
		if temp.next != nil {
			temp.next.pre = temp
		}
	} else {
		fmt.Println("sorry, è¦å é¤çidä¸å­å¨")
	}
}

func main() {
	//åå§å åå»ºä¸ä¸ªå¤´ç»ç¹
	head := &HeroNode{} //ç»é»è®¤å¼
	fmt.Println("head = ", head)

	//åå»ºä¸ä¸ªæ°çèç¹
	hero1 := &HeroNode{
		no:       1,
		name:     "å®æ±",
		nickname: "åæ¶é¨",
	}
	hero2 := &HeroNode{
		no:       2,
		name:     "å´ç¨",
		nickname: "å¼é£å¤é¨",
	}
	hero3 := &HeroNode{
		no:       2,
		name:     "å´ç¨3",
		nickname: "å¼é£å¤é¨3",
	}
	fmt.Println("hero1 = ", hero1)
	fmt.Println("hero2 = ", hero2)
	fmt.Println("hero3 = ", hero3)
	fmt.Println("æµè¯--------1----------")

	//3. å å¥æµè¯
	InsertHerNode2(head, hero2) //ä¼ å¥å¤´ç»ç¹åæ°èç¹
	InsertHerNode2(head, hero1) //ä¼ å¥å¤´ç»ç¹åæ°èç¹
	InsertHerNode2(head, hero3) //ä¼ å¥å¤´ç»ç¹åæ°èç¹
	ListHeroNode(head)          //æ¾ç¤º
	ListHeroNode2(head)         //æ¾ç¤º
	fmt.Println("æµè¯--------å é¤----------")

	//4. å é¤
	DelHerNode(head, 2)
	ListHeroNode(head) //æ¾ç¤º

}

```



**ç¼è¯ï¼**

```
PS C:\Users\smile\Desktop\åºåé¾\code\chapter05\ifelsedemo> go run .\main.go
head =  &{0   <nil> <nil>}
hero1 =  &{1 å®æ± åæ¶é¨ <nil> <nil>}
hero2 =  &{2 å´ç¨ å¼é£å¤é¨ <nil> <nil>}
hero3 =  &{2 å´ç¨3 å¼é£å¤é¨3 <nil> <nil>}
æµè¯--------1----------
æç¸åçèç¹ï¼é£ä¹ä¸å¯ä»¥æå¥
å¯¹ä¸èµ·ï¼å·²ç»å­å¨ 2
èç¹ä¿¡æ¯å¦ä¸:[ 1 å®æ± åæ¶é¨ ]===>
èç¹ä¿¡æ¯å¦ä¸:[ 2 å´ç¨ å¼é£å¤é¨ ]===>
ååé¾è¡¨ååæåºèç¹ä¿¡æ¯å¦ä¸:[ 2 å´ç¨ å¼é£å¤é¨ ]===>
ååé¾è¡¨ååæåºèç¹ä¿¡æ¯å¦ä¸:[ 1 å®æ± åæ¶é¨ ]===>
æµè¯--------å é¤----------
èç¹ä¿¡æ¯å¦ä¸:[ 1 å®æ± åæ¶é¨ ]===>
```





## Goè¯­è¨ç¯å½¢é¾è¡¨

**æå¥**

```go
func InsertNode(head *CatNode, newNode *CatNode) {
	//å¤æ­æ¯å¦ä¸ºç¬¬ä¸
	if head.next == nil {
		head.no = newNode.no
		head.name = newNode.name
		//æ³¨æï¼ä¸ä¸ªç»ç¹ä¹å¯ä»¥å½¢æç¯ç¶ç
		head.next = head //å½¢æä¸ä¸ªç¯ç¶
		//æ³¨æä¸å¯ä»¥æ¯Â·head.next = newNode,å ä¸ºheadæ¬èº«æä¸ä¸ªç©ºé´
		fmt.Println("ç¼å·ä¸º", head.no, "çç»ç¹å å¥")
		return
	}
	//æ­¤æ¶ä¸æ¯å¨ç¬¬ä¸ä½    --   ä½¿ç¨Â·ä¸´æ¶åéæ¾å°æåçç»ç¹
	temp := head
	for {
		if temp.next == head {
			//éåå°å¤´ç»ç¹ï¼è¯´æå·²ç»æ¾å°äº
			break
		}
		temp = temp.next
	}
	//å å¥å°ç¯ç¶é¾è¡¨ä¸­
	temp.next = newNode.next
	newNode.next = head

}
```



**æå°ç¯å½¢é¾è¡¨**

```go
//è¾åº    -- éè¦å¤´ç»ç¹
func show(head *CatNode) {
	temp := head
	fmt.Println("ç¯å½¢é¾è¡¨çæåµå¦ä¸:")
	if temp.next == nil {
		//ç©ºé¾è¡¨
		fmt.Println("æ¯ä¸ä¸ªç©ºé¾è¡¨")
	}
	for {
		fmt.Println("å½åèç¹çä¿¡æ¯ä¸º = ", temp, "no = ", temp.no, "name=", temp.name, "==>>")
		if temp.next == head {
			//è¯´æå°éå¤´
			break
		}
		temp = temp.next
	}
}
```



**å é¤ç¯å½¢é¾è¡¨ç»ç¹**

```go
//ç¯å½¢é¾è¡¨çå é¤
func del(head *CatNode, id int) {
	temp := head
	helper := head

	//å¦ææ¯ç©ºç»ç¹
	if temp == nil {
		fmt.Println("è¿æ¯ä¸ä¸ªç©ºçç¯å½¢é¾è¡¨æ æ³å é¤")
		return
	}

	//å¦ææ¯ä¸ä¸ªç»ç¹
	if temp.next == head {
		temp.next = nil
	}

	//å¦ææ¯ä¸¤ä¸ªä»¥ä¸çç»ç¹
	/*è®©helperæåç¯å½¢é¾è¡¨çæå*/
	for {
		if temp.next == head {
			//æ¾å°äºæå,è¯´ææ¯è¾å°æå,ä½æ¯æåæ²¡ææ¯è¾
			break
		}
		if temp.no == id {
			//æ¾å°  -- å¯ä»¥ç´æ¥å é¤
			//temp.next == nil
		}
		temp = temp.next        //ç§»å¨åæ¯è¾
		helper = helper.next    // ç§»å¨  ä¸æ¦æ¾å°è¦å é¤çç»ç¹
		helper.next = temp.next //å é¤ç»ç¹
	}
}
func main() {
	//åå§åå¤´ç»ç¹ï¼ç¯å½¢éè¡¨1)
	head := &CatNode{}

	//åå»º
	cat1 := &CatNode{
		no:   1,
		name: "tom",
	}
	fmt.Println("cat1.next = ", cat1.next)
	cat2 := &CatNode{2, "çäº", nil}
	cat3 := &CatNode{3, "å¼ ä¸", nil}
	cat4 := &CatNode{4, "æå", nil}
	cat5 := &CatNode{2, "çå­", nil}

	InsertNode(head, cat1) //æ·»å 
	InsertNode(head, cat2) //æ·»å 
	InsertNode(head, cat3) //æ·»å 
	InsertNode(head, cat4) //æ·»å 
	InsertNode(head, cat5) //æ·»å 
	show(head)             //è¾åº
	//å é¤æä½
	var a int
	fmt.Println("è¯·éæ©å é¤çæ¨¡å¼åè¾åºçå¯¹è±¡")
	fmt.Scanln(&a)
	del(head, a)
	show(head) //è¾åº
}
```





### å¨ä»£ç 

```go
package main

import (
	"fmt"
)

//å®ä¹ç»æä½
type CatNode struct {
	no   int //å®ä¹ç¼å·
	name string
	next *CatNode
}

func InsertNode(head *CatNode, newNode *CatNode) {
	//å¤æ­æ¯å¦ä¸ºç¬¬ä¸
	if head.next == nil {
		head.no = newNode.no
		head.name = newNode.name
		//æ³¨æï¼ä¸ä¸ªç»ç¹ä¹å¯ä»¥å½¢æç¯ç¶ç
		head.next = head //å½¢æä¸ä¸ªç¯ç¶
		//æ³¨æä¸å¯ä»¥æ¯Â·head.next = newNode,å ä¸ºheadæ¬èº«æä¸ä¸ªç©ºé´
		fmt.Println("ç¼å·ä¸º", head.no, "çç»ç¹å å¥")
		return
	}
	//æ­¤æ¶ä¸æ¯å¨ç¬¬ä¸ä½    --   ä½¿ç¨Â·ä¸´æ¶åéæ¾å°æåçç»ç¹
	temp := head
	for {
		if temp.next == head {
			//éåå°å¤´ç»ç¹ï¼è¯´æå·²ç»æ¾å°äº
			break
		}
		temp = temp.next
	}
	//å å¥å°ç¯ç¶é¾è¡¨ä¸­
	temp.next = newNode.next
	newNode.next = head

}

//è¾åº    -- éè¦å¤´ç»ç¹
func show(head *CatNode) {
	temp := head
	fmt.Println("ç¯å½¢é¾è¡¨çæåµå¦ä¸:")
	if temp.next == nil {
		//ç©ºé¾è¡¨
		fmt.Println("æ¯ä¸ä¸ªç©ºé¾è¡¨")
		return
	}
	for {
		fmt.Println("å½åèç¹çä¿¡æ¯ä¸º = ", temp, "no = ", temp.no, "name=", temp.name, "==>>")
		if temp.next == head {
			//è¯´æå°éå¤´
			break
		}
		temp = temp.next //åç§»
	}
}

//ç¯å½¢é¾è¡¨çå é¤
func del(head *CatNode, id int) {
	temp := head
	helper := head

	//å¦ææ¯ç©ºç»ç¹
	if temp == nil {
		fmt.Println("è¿æ¯ä¸ä¸ªç©ºçç¯å½¢é¾è¡¨æ æ³å é¤")
		return
	}

	//å¦ææ¯ä¸ä¸ªç»ç¹
	if temp.next == head {
		temp.next = nil
	}

	//å¦ææ¯ä¸¤ä¸ªä»¥ä¸çç»ç¹
	/*è®©helperæåç¯å½¢é¾è¡¨çæå*/
	for {
		if temp.next == head {
			//æ¾å°äºæå,è¯´ææ¯è¾å°æå,ä½æ¯æåæ²¡ææ¯è¾
			break
		}
		if temp.no == id {
			//æ¾å°  -- å¯ä»¥ç´æ¥å é¤
			//temp.next == nil
		}
		temp = temp.next        //ç§»å¨åæ¯è¾
		helper = helper.next    // ç§»å¨  ä¸æ¦æ¾å°è¦å é¤çç»ç¹
		helper.next = temp.next //å é¤ç»ç¹
	}
}
func main() {
	//åå§åå¤´ç»ç¹ï¼ç¯å½¢éè¡¨1)
	head := &CatNode{}

	//åå»º
	cat1 := &CatNode{
		no:   1,
		name: "tom",
	}
	fmt.Println("cat1.next = ", cat1.next)
	cat2 := &CatNode{2, "çäº", nil}
	cat3 := &CatNode{3, "å¼ ä¸", nil}
	cat4 := &CatNode{4, "æå", nil}
	cat5 := &CatNode{2, "çå­", nil}

	InsertNode(head, cat1) //æ·»å 
	InsertNode(head, cat2) //æ·»å 
	InsertNode(head, cat3) //æ·»å 
	InsertNode(head, cat4) //æ·»å 
	InsertNode(head, cat5) //æ·»å 
	show(head)             //è¾åº
	//å é¤æä½
	var a int
	fmt.Println("è¯·éæ©å é¤çæ¨¡å¼åè¾åºçå¯¹è±¡")
	fmt.Scanln(&a)
	del(head, a)
	show(head) //è¾åº
}

```

