由于 Java 类加载器的限制, 自定义的 java.* 的类是不会被加载进虚拟机的.   
因此对源码进行注释的时候务必不要影响到 class 内指令到 java 文件的代码行映射,  
避免造成 debug 时断点和实际执行的代码不一致的情况. 

为避免上述问题, 对源码注释时稍加约定
1. 对注释的翻译, 在原注释的末尾增加 /**/// 翻译的内容
2. 对具体代码行的注释, 在原代码行尾增加 /* 内容 */
3. 对某类的详细解读, 解读放置于单独的文件并在类定义的行尾增加 /* @doc doc/xxx.md */
