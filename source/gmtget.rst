.. index:: ! gmtget

gmtget
======

:官方文档: :ref:`gmt:gmtget`
:简介: 列出单个或多个GMT参数的当前值

选项
----

``<PARAMETER>``
    GMT的参数名，见 :ref:`doc:configurations` 。

    ``gmtset`` 后直接跟一个或多个参数名::

        $ gmt gmtget PS_MEDIA
        a4

        $ gmt get MAP_GRID_CROSS_SIZE_PRIMARY MAP_GRID_CROSS_SIZE_SECONDARY
        24p,Helvetica,black 16p,Helvetica,black fancy

``-G<defaultsfile>``
    读取指定的配置文件

    该命令寻找配置文件 ``gmt.conf`` 时的搜索优先顺序为::

        ./gmt.conf  > ~/.gmt/gmt.conf > ~/gmt.conf > ${GMTHOME}/share/conf/gmt.conf

``-L``
    输出时一行只输出一个返回值。

    一次指定多个参数名时，默认会将所有返回值输出在一行，各值之间以空格分隔。该选项会一行只输出一个返回值。

    ::

        $ gmt get FONT_TITLE FONT_LABEL MAP_FRAME_TYPE -L
        24p,Helvetica,black
        16p,Helvetica,black
        fancy
