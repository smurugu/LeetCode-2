### 1288.Remove-Covered-Intervals

将所有的区间按照左端点排序，如果左端点相同的话，优先处理大区间。

我们顺序处理某个区间i，假设为[a,b]：后面的区间j的左端点一定都比a晚，如果j的右端点也比b早的话，那么j一定就是被包含在i里面的。我们可能会遇到若干个这样的j，但区间j会越来越靠右。直至发现j的右端点比b晚，说明j已经跑出了i的覆盖范围，那么我们就把j当作i，重复之前的操作。
