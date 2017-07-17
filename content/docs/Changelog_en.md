+++
bref = ""
date = "2017-06-03T17:49:01+08:00"
description = "In English"
draft = false
title = "ChangeLog"
toc = true
weight = 15

+++


### 5.0.3 -2017-06-20

- Solve the `supportMethodsArguments` parameter problem. It is recommended to upgrade to the latest version.


### 5.0.2 - 2017-05-30

- `Page<E>` implements `Closeable` interface, in JDK7+ which can use the in `try ()` call, it will automatically call `PageHelper.clearPage ();`[#58](https://github.com/pagehelper/Mybatis-PageHelper/issues/58) 
- fixed: DB2 paging must be specified sub-query alias, or an exception will occur [#52](https://github.com/pagehelper/Mybatis-PageHelper/issues/52)
- fixed `page.size() == 0` then `pageInfo.isIsLastPage()` is `false` [#50](https://github.com/pagehelper/Mybatis-PageHelper/issues/50)


### 5.0.1 - 2017-04-23
- Add the new parameter `countColumn` used to configure the automatic count column, the default value `0`, that is, `count(0).
- The `Page` class is also added with the `countColumn` parameter, which can be configured for a specific query.
- Modify the document display problem, by liumian* [PR #30](https://github.com/pagehelper/Mybatis-PageHelper/pull/30)
- Resolved sqlserver2012 paging error [42](https://github.com/pagehelper/Mybatis-PageHelper/issues/42)

### 5.0.0 - 2017-01-02

- Use Use [QueryInterceptor spec](https://github.com/pagehelper/Mybatis-PageHelper/blob/master/src/main/java/com/github/pagehelper/QueryInterceptor.java) to handle paging logic
- New pagination plugin interceptor `com.github.pagehelper.PageInterceptor`
- New `Dialect` `PageHelper` is a special implementation class, the previous function is implemented in more user-friendly ways
- New pagination plugin only a `dialect` parameter, the default `dialect` is `PageHelper`
- `PageHelper` continue to support previously provided parameters, Among the latest to use the document has been fully updated
- `PageHelper` has a `helperDialect` parameter which is the same functional as the previous `dialect`
- Added paging implementation based on pure `RowBounds` and `PageRowBounds`,
  in `com.github. pagehelper. dialect. rowbounds` package, it is used as `dialect` Parameter sample implementation, more detailed documentation will be added later
- Removed inappropriate orderby functions that appear in pagination plugin. It will provide a separate sort plug-ins in the future
- Remove `PageHelper` are less commonly used methods
- A new document, an important part of the update has been mentioned in the changelog, provides the English version of this document
- fix bug [#149](http://git.oschina.net/free/Mybatis_PageHelper/issues/149)
- renamed Db2RowDialect to Db2RowBoundsDialect
- All thrown exceptions being replaced by PageException

## Older Changelogs are written in Chinese
You can [view here](https://github.com/pagehelper/Mybatis-PageHelper/blob/master/wikis/zh/Changelog.md)
