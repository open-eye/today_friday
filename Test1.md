### Test1

应用反射在Controller层，太臃肿，一次请求长长的if else，优化后，baseServlet重写httpSerlvet的doGet方法，根据请求的method参数，反射执行对应的method方法

