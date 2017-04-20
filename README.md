# ZZCollectionView
仿购物车勾选size和color
在添加商品到购物车时，通常需要选择商品属性，比如颜色和尺码。使用collectionView来实现时，我们需要在颜色分类和尺码分类中各选择一个选项，并且选中的选项有自己的呈现效果，这里我的实现思路是这样的：
1）每个section用一个属性记录被选中的index \n
2）在cellForItem中根据（indexPath.item == 该section的全局index）来设置cell.selected \n
3）在selectItem方法中设置各section的全局index之后reload collectionView \n
4）在cell中重写setSelected方法 设置选中和非选中效果 \n
