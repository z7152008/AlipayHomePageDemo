# swift-AlipayHomePageDemo
仿支付宝首页滚动效果

![snapshot](https://github.com/GorXion/AlipayHomePageDemo/blob/master/alipay_home.gif)

## 主要思路:

``` objc

  // 一个scrollView容器添加两个子view
  scrollView.addSubview(tableView)
  scrollView.addSubview(collectionView)
  
  // 禁止中间的collectionView滚动
  collectionView.isScrollEnabled = false
        
  // 移除父scrollView的所有手势
  scrollView.gestureRecognizers?.forEach({
    scrollView.removeGestureRecognizer($0)
  })
        
  // 将tableView的手势添加到父scrollView上
  tableView.gestureRecognizers?.forEach({
    scrollView.addGestureRecognizer($0)
  })
```
