# AncientChinese
书生文
=====
## 文件说明
    带{}的单词表示需要替换的文本
### 文件相关接口
    111.230.253.18/api/file/get/{fileid}
    方法:get
    参数说明：
        fileid：文件的id
    结果类型：
        文件
### 字帖相关接口
    111.230.253.18/api/copybook/typelist
    作用:获取字帖类型列表
    方法:get
    参数说明：
        无
    结果类型：
        数组
    结果说明：
        {
            "TypeId": 0,
            "TypeName": "古文"
        }
        
    111.230.253.18/api/copybook/list
    作用:获取字帖列表
    方法:get
    参数说明：
        无
    结果类型：
        数组
    结果说明：
        {
            "Id": "c50b6067-dbac-4a43-83c2-3b4b4918aea6",
            "Title": "为有",
            "BookType": "唐诗",
            "Author": "李商隐",
            "FontType": "繁体",
            "Content": "    为有云屏无限娇，凤城寒尽怕春宵。\n    无端嫁得金龟婿，辜负香衾事早朝。 "
        }
     
    111.230.253.18/api/copybook/list?type={typeId}
    作用:通过字帖类型获取字帖列表
    方法:get
    参数说明：
        typeId:字帖类型ID
        
    111.230.253.18/api/copybook/detail/{id}
    作用:获取字帖的图片列表数据
    方法:get
    参数说明：
        id：字帖的id
    结果类型：
        数组
    结果说明：
        文件的id
### 名家欣赏相关接口
    111.230.253.18/api/appreciate/authorslist
    作用:获取作者列表
    方法:get
    参数说明：
        无
    结果类型：
        数组
        
    111.230.253.18/api/appreciate/timeslist
    作用:获取朝代列表
    方法:get
    参数说明：
        无
    结果类型：
        数组
        
    111.230.253.18/api/appreciate/authors?authors={authorName}
    作用:获取该作者的作品
    方法:get
    参数说明：
        authorName:作者姓名
    结果类型：
        数组
        
    111.230.253.18/api/appreciate/times?times={times}
    作用:获取该朝代的作品
    方法:get
    参数说明：
        times:朝代名
    结果类型：
        数组
    
    111.230.253.18/api/appreciate/list
    作用:获取所有作品
    方法:get
    参数说明：
        无
    结果类型：
        数组
    
    111.230.253.18/api/appreciate/detail/{id}
    方法:get
    参数说明：
        id：名家欣赏的id
    结果类型：
        数组
    结果说明：
        文件的id
        
### 字典相关接口
    111.230.253.18/api/Font/FontType
    方法:get
    参数说明：
        无
    结果类型：
        数组
    结果说明：
        字体类型
        
    111.230.253.18/api/Font/FontDetail?typeId={typeId}
    方法:get
    参数说明：
        typeId:字体类型
    结果类型：
        数组
    结果说明：
        该字体类型所有的字及其对应的文件id
        
        
    111.230.253.18/api/Font/FontDetail?type={type}
    方法:get
    参数说明：
        type:字体类型
    结果类型：
        数组
    结果说明：
        该字体类型所有的字及其对应的文件id
    
    111.230.253.18/api/Font/word?search={word}
    方法:get
    参数说明：
        word:要搜索的字
    结果类型：
        数组
    结果说明：
        该字对应的所有的字及其对应的文件id，查无此字返回一个空数组
