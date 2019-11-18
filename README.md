# JAVA实验报告
班级：计G191
姓名 : 崔长江
学号：2019322045

实验目的:

掌握字符串String及其使用方法
掌握异常处理结构

要求：

利用已学的字符串处理只是完成《长歌行》古诗的整齐对齐工作，写出功能函数，并运行：
1.每7个汉字加一个标点，奇书”，“，偶数”。“
2.允许提供输入参数，统计古诗中某个字的出现次数
3.考虑操作中可能的异常

实验过程：
创建字符串函数，截取每一段加入符号的字符串，写入一个新的String，添加查找方法，加入可能异常和处理


实验流程图：


核心代码：

		String str2 = "";
		for (int i = 0; i < str.length(); i++) {
			if (i * 7 + 7 > str.length()) {
				str2 += str.substring(i * 7, str.length());
				break;
			}
			if ((i * 7) % 2 == 0) {
				str2 += str.substring(i * 7, i * 7 + 7) + ",";
			} else {
				str2 += str.substring(i * 7, i * 7 + 7) + "." + "\n";
			}
		}
		System.out.println(new StringBuilder(str2).toString());
		String a = "一";
		int count = count(str, a);
		System.out.println(a +  "在其中出现的次数为:"
				+ count);
	}

	public static int count(StringBuilder str, String findStr) {
		int count = 0;
		int index = 0;
		while ((index = str.indexOf(findStr, index)) != -1) {
			index = index + findStr.length();
			count++;
		}
		return count;

运行截图：

编程感想：
这次试验总体来说还是不错的，之前有一些java基础，但是好久没接触，有些忘记了，截取字符串出现一些问题，以后看来需要多练习，一些基础都没有熟悉，希望自己在今后学习中多多注意这些细节。
