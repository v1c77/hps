# hps
 list process hugepage usage


- assmue the hugepage dev path `/dev/hugepage`
- dev on centos7 and fedroa 33

list hugepage of every processes. 

inspaird by the command pipline below.

```
grep -B 11 'KernelPageSize:     2048 kB' /proc/22466/smaps | grep "^Size:" | awk 'BEGIN{sum=0}{sum+=$2}END{print sum/1024}'
```
