***
# 最传统 C 的方式及问题

- 比如业务里有一个 Group, Group 里又有 Student, Student 里又有 name 作为名字

1. Students 和 Groups 都在堆上
```cpp
typedef{
	char* name[50];
} Student;

typedef {
    Student* students[1];
} Group；

int main(){

	//在堆上创建 grp
	Group* grp = (Group*)malloc(sizeof(Group));
	
	//在堆上创建 stu1 
	Student* stu1 = (Student*)malloc(sizeof(Student));
	
	//初始化 stu 和 grp
	strcpy(stu1->name, "张三");
	grp->students[0] = stu1;
	 
	// do something
	
	
	//程序结束，释放内存
	free(stu1);
	free(grp);
	
}
```
我们看到，不仅要释放 grp，grp 内的 stu 我们也要手动释放

如果不想手动释放 Stu 我们可以修改 Class ，让其保存 Student 数组而不是指针数组
```cpp
typedef{
	char* name[50];
} Student;

typedef {
    Student students[1];
} Group；



```

