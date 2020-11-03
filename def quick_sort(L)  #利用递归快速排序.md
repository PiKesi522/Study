def quick_sort(L):  #利用递归快速排序
    if len(L) <= 1: #脱出条件放在首位
        return L;
    a = L[0];       #将首位作为判断依据，为了防止特殊情况，可以使用随机位
    L1 =[];L2=[];   #创建新列表用以存放比 判断数 大或者小的数字
    for e in L:
        if(e <= a):
            L1.append(e);
        else:
            L2.append(e);
        return quick_sort(L1) + a + quick_sort(L2);