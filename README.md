## Setup

Two servers equipped with ConnectX-6 adapter cards connected back-to-back.

## Compilation

Download the attached C files below to your servers and compile as follows:

```bash
gcc -o receiver mp_rq.c -libverbs
gcc -o sender mp_sq.c -libverbs
```
 
## Execution Example

Once running the application, the following output will be received on the sender and the receiver sides.

### Sender

```bash
gcc -o sender mp_sq.c -libverbs

sudo ./sender
```

The results should be

```bash
completed message 61549056
completed message 61553045
completed message 61554678
...
```

### Receiver

```bash
gcc -o receiver mp_rq.c -libverbs

sudo ./receiver
```

The results should be

```bash
message 1 received size 98
message 2 received size 98
message 3 received size 98
...
```

## Reference

https://support.mellanox.com/s/article/raw-ethernet-programming--basic-introduction---code-example