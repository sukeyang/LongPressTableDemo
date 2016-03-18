# LongPressTableDemo
长按删除,tableviewCell
#目的
适用于一些页面,滑动事件被占用的情况,还的去做滑动删除
#集成方法
加入demo中的`LongPressTable`文件夹
```
#import "UITableView+LongPressTable.h"
#import "UITableViewDataSource_LongPreeable.h"
```
添加代码
```
tableView.longPressTableAble = YES;
```
实现协议`UITableViewDataSource_LongPreeable`为了保证cel高度不一样情况下正常运作
```
-(CGFloat)tableView:(UITableView *)tableView heightForRowAtIndexPath:(NSIndexPath *)indexPath
```
集成成功

使用完最好进行
```
- (void)dealloc{
    m_tableView.longPressTableAble = NO;
}
```