

[toc]

ð¶âð«ï¸goè¯­è¨å®æ¹ç¼ç¨æåï¼[https://golang.org/#](https://golang.org/#)  

>   goè¯­è¨çå®æ¹ææ¡£å­¦ä¹ ç¬è®°å¾å¨ï¼æ¨èå»å®ç½å­¦ä¹ 

ð¶âð«ï¸æçå­¦ä¹ ç¬è®°ï¼github: [https://github.com/3293172751/golang-rearn](https://github.com/3293172751/golang-rearn)

---

**åºåé¾ææ¯ï¼ä¹ç§°ä¹ä¸ºåå¸å¼è´¦æ¬ææ¯ï¼**ï¼æ¯ä¸ç§äºèç½æ°æ®åºææ¯ï¼å¶ç¹ç¹æ¯å»ä¸­å¿åï¼å¬å¼éæï¼è®©æ¯ä¸ä¸ªäººåå¯åä¸çæ°æ®åºè®°å½

>   â¤ï¸ððå³äºåºåé¾ææ¯ï¼å¯ä»¥å³æ³¨æï¼å±åå­¦ä¹ æ´å¤çåºåé¾ææ¯ãåå®¢[http://nsddd.top](http://nsddd.top)

---

 # chanç¯å½¢éå åè¿ååº

# 1 ç¯å½¢ç¼å²åº
## 1.1 ç¯å½¢ç¼å²åºç»æ
â       ç¯å½¢ç¼å²åºéå¸¸æä¸ä¸ªè¯»æéåä¸ä¸ªåæéãè¯»æéæåç¯å½¢ç¼å²åºä¸­å¯è¯»çæ°æ®ï¼åæéæåç¯å½¢ç¼å²åºä¸­å¯åçç¼å²åºãéè¿ç§»å¨è¯»æéååæéå°±å¯ä»¥å®ç°ç¼å²åºçæ°æ®è¯»åååå¥ãå¨éå¸¸æåµä¸ï¼ç¯å½¢ç¼å²åºçè¯»ç¨æ·ä»ä»ä¼å½±åè¯»æéï¼èåç¨æ·ä»ä»ä¼å½±ååæéãå¦æä»ä»æä¸ä¸ªè¯»ç¨æ·åä¸ä¸ªåç¨æ·ï¼é£ä¹ä¸éè¦æ·»å äºæ¥ä¿æ¤æºå¶å°±å¯ä»¥ä¿è¯æ°æ®çæ­£ç¡®æ§ãå¦ææå¤ä¸ªè¯»åç¨æ·è®¿é®ç¯å½¢ç¼å²åºï¼é£ä¹å¿é¡»æ·»å äºæ¥ä¿æ¤æºå¶æ¥ç¡®ä¿å¤ä¸ªç¨æ·äºæ¥è®¿é®ç¯å½¢ç¼å²åºã

## 1.2 ç¯å½¢ç¼å²åºä¸ç§è¯»åå®ç°æºå¶
ä¸è¬çï¼åå½¢ç¼å²åºéè¦4ä¸ªæé

å¨åå­ä¸­å®éå¼å§ä½ç½®ï¼

**å¨åå­ä¸­å®éç»æä½ç½®ï¼ä¹å¯ä»¥ç¨ç¼å²åºé¿åº¦ä»£æ¿ï¼**

**å­å¨å¨ç¼å²åºä¸­çæææ°æ®çå¼å§ä½ç½®ï¼è¯»æéï¼ï¼**

**å­å¨å¨ç¼å²åºä¸­çæææ°æ®çç»å°¾ä½ç½®ï¼åæéï¼ã**

ç¼å²åºæ¯æ»¡ãææ¯ç©ºï¼é½æå¯è½åºç°è¯»æéä¸åæéæååä¸ä½ç½®ï¼

ç¼å²åºä¸­æ»æ¯æä¸ä¸ªå­å¨ååä¿ææªä½¿ç¨ç¶æãç¼å²åºæå¤å­å¥ï¼size-1ï¼ä¸ªæ°æ®ãå¦æè¯»åæéæååä¸ä½ç½®ï¼åç¼å²åºä¸ºç©ºãå¦æåæéä½äºè¯»æéçç¸é»åä¸ä¸ªä½ç½®ï¼åç¼å²åºä¸ºæ»¡ã

![img](https://s2.loli.net/2022/03/20/6EgmtVuvlj2YMxU.jpg)



## 2 chanåé¨æ°æ®ç»æ

### 2.1 chançæ°æ®ç»æ

**chanå®è´¨æ¯ä¸ªç¯å½¢ç¼å²åºï¼å¤å ä¸ä¸ªæ¥åèåç¨éååä¸ä¸ªåéèåç¨éå**

```
buf      ï¼ç¯å½¢ç¼å²åº
sendx ï¼ç¨äºè®°å½bufè¿ä¸ªå¾ªç¯é¾è¡¨ä¸­çåéçindex
recvx  ï¼ç¨äºè®°å½bufè¿ä¸ªå¾ªç¯é¾è¡¨ä¸­æ¥æ¶çindex
recvq  ï¼æ¥åèåç¨éå
sendq ï¼åéèåç¨éå
lock    ï¼äºæ¥é
```


### 2.2 æç¼å²åºåæ ç¼å²åºchançåºå«
##### 2.2.1 æ ç¼å²chanæ°æ®åæ­¥è¿ç¨åsudogç»æ
åå»ºä¸ä¸ªåéèåè¡¨åæ¥æ¶èåè¡¨é½ä¸ºç©ºç channelã
ç¬¬ä¸ä¸ªåç¨å channel åéåéçå¼
channel ä»æ± ä¸­è·åä¸ä¸ªsudogç»æä½åéï¼ç¨äºè¡¨ç¤ºåéèãsudog ç»æä½ä¼ä¿æå¯¹åéèæå¨åç¨çå¼ç¨ï¼ä»¥ååéåéçå¼ç¨ã
åéèå å¥sendqéåã
åéèåç¨è¿å¥ç­å¾ç¶æã
ç¬¬äºä¸ªåç¨å°ä» channel ä¸­è¯»åä¸ä¸ªæ¶æ¯
channel å°sendqåè¡¨ä¸­ç­å¾ç¶æçåéèåºéåã
chanel ä½¿ç¨memmoveå½æ°å°åéèè¦åéçå¼è¿è¡æ·è´ï¼åè£å¥sudogç»æä½ï¼åä¼ éç» channel æ¥æ¶èçæ¥æ¶åéã
å¨ç¬¬äºæ­¥ä¸­è¢«æèµ·çç¬¬ä¸ä¸ªåç¨å°æ¢å¤è¿è¡å¹¶éæ¾ç¬¬ä¸æ­¥ä¸­è·åçsudogç»æä½ã

##### 2.2.1 æç¼å²chan

æç¼å²chanå®è´¨æ¯ä½¿ç¨äºå®æ´çç¯å½¢ç¼å²åºï¼åªè¦ç¼å²åºæç©ºé²ï¼ååéèæ éè¿å¥ç­å¾éåï¼ç´æ¥å°æ°æ®æ¾å¥ç¯å½¢ç¼å²åºä¸­ï¼å¦æç¼å²åºææ°æ®ï¼æ¥åèæ éè¿å¥ç­å¾éåï¼ç´æ¥ä»ç¯å½¢ç¼å²åºä¸­è·åæ°æ®ã

## 3 å³é®æºç åæ

### 3.1 chanæ°æ®ç»ææºç 

```go
type hchan struct {
	qcount   uint           // total data in the queue
	dataqsiz uint           // size of the circular queue
	buf      unsafe.Pointer // points to an array of dataqsiz elements
	elemsize uint16
	closed   uint32
	elemtype *_type // element type
	sendx    uint   // send index
	recvx    uint   // receive index
	recvq    waitq  // list of recv waiters
	sendq    waitq  // list of send waiters
// lock protects all fields in hchan, as well as several
// fields in sudogs blocked on this channel.
//
// Do not change another G's status while holding this lock
// (in particular, do not ready a G), as this can deadlock
// with stack shrinking.
lock mutex
}
```
### 3.2 sudogæ°æ®ç»ææºç 

```go
// sudog represents a g in a wait list, such as for sending/receiving
// on a channel.
//
// sudog is necessary because the g â synchronization object relation
// is many-to-many. A g can be on many wait lists, so there may be
// many sudogs for one g; and many gs may be waiting on the same
// synchronization object, so there may be many sudogs for one object.
//
// sudogs are allocated from a special pool. Use acquireSudog and
// releaseSudog to allocate and free them.
type sudog struct {
	// The following fields are protected by the hchan.lock of the
	// channel this sudog is blocking on. shrinkstack depends on
	// this for sudogs involved in channel ops.
g 		*g
// isSelect indicates g is participating in a select, so
// g.selectDone must be CAS'd to win the wake-up race.
isSelect bool
next     *sudog
prev     *sudog
elem     unsafe.Pointer // data element (may point to stack)
 
// The following fields are never accessed concurrently.
// For channels, waitlink is only accessed by g.
// For semaphores, all fields (including the ones above)
// are only accessed when holding a semaRoot lock.
 
acquiretime int64
releasetime int64
ticket      uint32
parent      *sudog // semaRoot binary tree
waitlink    *sudog // g.waiting list or semaRoot
waittail    *sudog // semaRoot
c           *hchan // channel
}
```
### 3.3 chançæé è¿ç¨

```go
func makechan(t *chantype, size int) *hchan {
	elem := t.elem
// compiler checks this but be safe.
if elem.size >= 1<<16 {
	throw("makechan: invalid channel element type")
}
if hchanSize%maxAlign != 0 || elem.align > maxAlign {
	throw("makechan: bad alignment")
}
 
mem, overflow := math.MulUintptr(elem.size, uintptr(size))
if overflow || mem > maxAlloc-hchanSize || size < 0 {
	panic(plainError("makechan: size out of range"))
}
 
// Hchan does not contain pointers interesting for GC when elements stored in buf do not contain pointers.
// buf points into the same allocation, elemtype is persistent.
// SudoG's are referenced from their owning thread so they can't be collected.
// TODO(dvyukov,rlh): Rethink when collector can move allocated objects.
var c *hchan
switch {
case mem == 0:
	// Queue or element size is zero.
	c = (*hchan)(mallocgc(hchanSize, nil, true))
	// Race detector uses this location for synchronization.
	c.buf = c.raceaddr()
case elem.ptrdata == 0:
	// Elements do not contain pointers.
	// Allocate hchan and buf in one call.
	c = (*hchan)(mallocgc(hchanSize+mem, nil, true))
	c.buf = add(unsafe.Pointer(c), hchanSize)
default:
	// Elements contain pointers.
	c = new(hchan)
	c.buf = mallocgc(mem, elem, true)
}
 
c.elemsize = uint16(elem.size)
c.elemtype = elem
c.dataqsiz = uint(size)
 
if debugChan {
	print("makechan: chan=", c, "; elemsize=", elem.size, "; dataqsiz=", size, "\n")
}
return c
}
```

å¯ä»¥çå°ï¼å¦æä¸ä¼ å¥sizeæsize=0ï¼åæ²¡æä¸ºç¯å½¢ç¼å²åºåéåå­ï¼èä½chanç»æåéåå­

### 3.4 æ ç¼å²æ¶å

```go
// Sends and receives on unbuffered or empty-buffered channels are the
// only operations where one running goroutine writes to the stack of
// another running goroutine. The GC assumes that stack writes only
// happen when the goroutine is running and are only done by that
// goroutine. Using a write barrier is sufficient to make up for
// violating that assumption, but the write barrier has to work.
// typedmemmove will call bulkBarrierPreWrite, but the target bytes
// are not in the heap, so that will not help. We arrange to call
// memmove and typeBitsBulkBarrier instead.

func sendDirect(t *_type, sg *sudog, src unsafe.Pointer) {
	// src is on our stack, dst is a slot on another stack.
	// Once we read sg.elem out of sg, it will no longer
	// be updated if the destination's stack gets copied (shrunk).
	// So make sure that no preemption points can happen between read & use.
	dst := sg.elem
	typeBitsBulkBarrier(t, uintptr(dst), uintptr(src), t.size)
	// No need for cgo write barrier checks because dst is always
	// Go memory.
	memmove(dst, src, t.size)

}

func recvDirect(t *_type, sg *sudog, dst unsafe.Pointer) {
	// dst is on our stack or the heap, src is on another stack.
	// The channel is locked, so src will not move during this
	// operation.
	src := sg.elem
	typeBitsBulkBarrier(t, uintptr(dst), uintptr(src), t.size)
	memmove(dst, src, t.size)
}
```



------------------------------------------------
