## Node.contains
* Node.contains() 返回的是一个布尔值,来表示传入的节点是否为该节点的后代节点。
* node.contains(otherNode)
* node 是否包含otherNode节点
* otherNode是否是node的后代节点。
* 如果otherNode是node的后代节点或是node节点本身,则返回true,否则返回false
## Node.appendChild
* Node.appendChild() 方法将一个节点添加到指定的父节点的子节点列表末尾。
* appendChild方法会把要插入的这个节点引用作为返回值返回。
* 如果被插入的节点已经存在于当前的文档的文档树中,则那个节点会首先从原来的位置移除,然后再插入到新的位置。
* 如果你需要保留这个子节点在原先的位置显示,则你需要先用Node.cloneNode方法复制出一个节点的副本,然后再插入到新的位置。