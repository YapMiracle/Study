# 我是从11.13开始学的

## 11.14开始记录。

1、学习了Macro这个变态的语法

```rust
macro_rules! my_macro{
    ($a:expr)=>{
        "Hello ".to_string() + $a
    }
}
```

2、还有就是变量的使用权的转移

```rust
let x=5;
let y=x;//这里就转移了
```

3、最后变量与常量没有理解，第二天再搞

## 11.15 星期二

1、if 结构语法

2、简单的函数

3、所有权和借用，没有理解号，费头发的地方来了😭

## 11.16 星期三

1、所有权和借用，理解了一点

```rust
// Should not take ownership
fn get_char(data1: &String) -> char {//借用&
    data1.chars().last().unwrap()
}		//data1没有失效，&只是暂时借用；相当于使用完毕，物归原主，有借【有】还
fn get_return(data:String) ->String{//拥有所有权
    println!("{}", data);
    data
}		//通过返回值将所有权归还，有借【有】还
// Should take ownership
fn string_uppercase(mut data: String) {//拥有所有权
    data = data.to_uppercase();

    println!("{}", data);
}		//data失效了，有借【无】还
```

2、现在是第二天0.15，要睡了，就看了这一个知识点