## Linux 


## ls
ls는 List의 약자로 디렉토리에 있는 파일 목록 확인
```
$ ls
testfile1 testfile2 testfile3
```
## cd
cd는 Change Directory의 약자로 디렉토리를 이동하는 명령이다.
```
cd
```
## pwd
pwd는 Print Working Directory의 약자로 현재 작업중인 디렉토리의 정보를 출력한다.
```
$ pwd
/root
```
## cp
cp는 Copy Pile의 약자로 파일이나 디렉토리의 정보를 복사한다.
```
cp$ ls
testdir/  testfile

$ cp testfile1 testfile_cp
$ ls
testdir/  testfile  testfile_cp$ cp -r testdir testdir_cp
$ ls
testdir/  testdir_cp/  testfile  testfile_cp
```
디렉토리를 복사할 때는 -r 옵션을 주어야 한다.
```
$ cp -r testdir testdir_cp
$ ls
testdir/  testdir_cp/  testfile  testfile_cp
```

## rm
rm은 remove의 약자로 파일이나 디렉토리를 삭제합니다.
```
$ rm abc.txt -> 해당 파일 삭제
$ rm -f abc.txt -> 삭제 시 확인하지 않고 바로 삭제(f는 force의 약자)
$ rm -rf abc ->  r 옵션과 f 옵션을 합친 것으로 abc 디렉터리와 그 아래에 있는 하위 디렉터리를 강제로 전부 삭제
```
## mv
mv는 move의 약자로 파일이나 디렉토리의 이름을 변경하거나 다른 디렉토리로 옮길 때 사용한다.
```
$ mv abc.txt /etc/sysconfig/
$ mv aaa bbb ccc ddd
$ mv abc.txt www.txt
```

## mkdir
mkdir은 Make Directory의 약자로 새로운 디렉토리를 생성한다.
```
$ mkdir abc
$ mkdir testdir
```

## rmdir
rmdir은 Remove Directory의 약자로 디렉토리를 삭제한다. 해당 디렉토리의 삭제 권한이 있어야 하며 티렉토리는 비어 있어야 합니다. 비어 있지 않다면 ```rm -r```명령을 실행해야 한다.

```
$ rmdir abc    →    /abc 디렉터리를 삭제
```

## cat
cat은 concatenate의 약자로 파일 내용을 화면에 출력한다.
```
$ cat a.txt    → a.txt 파일의 내용을 화면에 출력
```
단순히 파일의 내용을 출력하기도 하고, 파일 여러개를 합쳐서 하나의 파일로도 만들 수 있다.