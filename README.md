# grpc-go-2

We modified gRPC-go-83f9def5feb388c4fd7e6586bd55cf6bf6d46a01 by doing the two changes:

1. We replace all 'func (s) Test' with 'func Test' by executing the following command. 

```
$ grep -rl 'func (s) Test' ./ | xargs sed -i 's/func (s)/func/g'
```

2. We comment out the body of ```func check(efer Errorfer, timeout time.Duration)``` in file internal/leakcheck/leakcheck.go.



