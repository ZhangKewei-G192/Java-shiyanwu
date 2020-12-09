# Java-shiyanwu
实验五实验报告

#计192 张可为 学号：2019310186

#阅读程序 
package 实验五;
import java.util.Scanner;
import java.io.*;

public class Test {
    public static void main(String args[]) {
        student xuesheng = new student();
        System.out.println("输入姓名，性别，年龄，学号");
        Scanner s = new Scanner(System.in);
        String name = s.nextLine();
        String sex = s.nextLine();
        int age = s.nextInt();
        int number = s.nextInt();
        xuesheng.setGraduate(name, sex, age, number);

        try {
            FileReader fileReader = new FileReader("E:\\test.txt");
            BufferedReader bufferedReader = new BufferedReader(fileReader);
            Writer writer = new FileWriter(new File("E:\\123.txt"));
            String str = bufferedReader.readLine();
            String regex = "(.{7})";
            str = str.replaceAll(regex, "$1，");
            StringBuffer x = new StringBuffer(str);
            for (int  i = 15; i <289; i = i + 17) {
                x.replace(i, i + 1, "。\n");
            }
            System.out.println(x);
            writer.write(String.valueOf(xuesheng));
            writer.write("\n");
            writer.write(String.valueOf(x));
            bufferedReader.close();
            fileReader.close();
            writer.close();
        } catch (IOException e) {
            e.printStackTrace();
        } catch (Exception e) {
            System.out.println("出现错误!");
        }
    }
}
        
#实验目的 
掌握字符串String及其方法的使用

掌握文件的读取/写入方法

掌握异常处理结构


#实验过程

设计学生类；

采用交互式方式实例化某学生；

设计程序完成上述的业务逻辑处理，并且把“古诗处理后的输出”结果存储到学生基本信息所在的文本文件A中。

文件A包括两部分内容：

一是学生的基本信息；

二是学生处理后的作业信息，该作业的业务逻辑内容是：利用已学的字符串处理知识编程完成《长恨歌》古诗的整理对齐工作，写出功能方法，实现如下功能：

每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”
允许提供输入参数，统计古诗中某个字或词出现的次数
输入的文本来源于文本文件B读取，把处理好的结果写入到文本文件A
考虑操作中可能出现的异常，在程序中设计异常处理程序

#核心方法 

1.方法调用

2.文件读取/写入

3.分词方法设计

#实验感想 通过本次实验我学习了，方法的调用，文件读取/写入，分词方法设计以及使用。 有很多收获，增加了对Java的学习欲望。
