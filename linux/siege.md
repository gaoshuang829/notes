1����ȡԴ�룬siege-lastest.tar.gz��һֱ�����µ�  
```
 wget http://download.joedog.org/siege/siege-latest.tar.gz  
```
2����ѹ��װ��
```
tar -xvf siege-latest.tar.gz
```
3�����뵽siege Ŀ¼,��ǰ�汾��4.0.2���Կ�cd����cd siege-4.0.2
```
cd siege-4.0.2
```
4����siege-4.0.2Ŀ¼�£�����./configure��������������Ϣ�������������������Ŀ��ļ�
```
./configure
```
5������Ͱ�װ,make������һ���������ļ���make install�����ɵĶ������ļ���װ��ָ����Ŀ¼�¡�Ĭ�ϵİ�װĿ¼��/usr/local/bin/
```
make
sudo make install
```
6���鿴siege�汾��
```
siege -V OR  siege --version
```
�鿴�汾��Ϣ��Ĭ�����ò�����
|������                            |ֵ                  |���ı�ע           |
|----------------------------------|--------------------------------|--------------------|
|version:                          |4.0.2                           |�汾��|
|verbose:                          |true                            ||
|color:                            |true                            ||
|quiet:                            |false                           ||
|debug:                            |false                           ||
|protocol:                         |HTTP/1.1                        ||
|HTML parser:                      |enabled                         ||
|get method:                       |HEAD                            ||
|connection:                       |close                           ||
|concurrent users:                 |25                              | ָ���û�����|
|time to run:                      |n/a                             |����ʱ�䣬Ĭ��Ϊn/a��û��ָ��|
|repetitions:                      |n/a                             |ÿ���û�������������Ĭ��Ϊn/a, û��ָ��|
|socket timeout:                   |30                              ||
|accept-encoding:                  |*                               ||
|delay:                            |0.500 sec                       ||
|internet simulation:              |false                           ||
|benchmark mode:                   |false                           ||
|failures until abort:             |1024                            |����һ������ֹͣ����|
|named URL:                        |none                            ||
|URLs file:                        |/usr/local/etc/urls.txt         ||
|thread limit:                     |255                             ||
|logging:                          |false                           ||
|log file:                         |/usr/local/var/log/siege.log    ||
|resource file:                    |/home/ubuntu/.siege/siege.conf  |��Դ�ļ���Ҳ�����������ϲ������ļ����ļ�·��Ϊ/usr/local/etc/siegerc|
|timestamped output:               |false                           ||
|comma separated output:           |false                           ||
|allow redirects:                  |true                            ||
|allow zero byte data:             |true                            ||
|allow chunked encoding:           |true                            ||
|upload unique files:              |true                            ||
|no-follow:
 - ad.doubleclick.net
 - pagead2.googlesyndication.com
 - ads.pubsqrd.com
 - ib.adnxs.com




