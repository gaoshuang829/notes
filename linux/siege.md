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
|no-follow:                        |                                ||
| - ad.doubleclick.net             | ||
| - pagead2.googlesyndication.com  |||
| - ads.pubsqrd.com                |||
| - ib.adnxs.com                   |||


```
Siege���õĲ��������¼�����

-c ���� --concurrent=NUM : ����ָ����������
-r ���� --reps=NUM       : ����ָ���ظ�����
-d ���� --delay=NUM      : ����ָ���ӳ�ʱ��
-f ���� --file=FILE      : ����ָ��URL�б���ļ�������һ�ζԶ��·�����в���
-t ���� --time=NUMm      : ����ָ�����Գ���ʱ�䡣���磺 -t10S (10��)  -t5M(5����)  -t1H(1Сʱ)
-l ���� --log[=FILE]     : ���ڼ�¼�����־

```
������⣺  
-C,��????onfig ����Ļ�ϴ�ӡ��ʾ����ǰ������,�����ǰ��������������ļ�$HOME/.siegerc��,���Ա༭����Ĳ���,����ÿ��siege ���ᰴ��������.  
-v ����ʱ�ܿ�����ϸ��������Ϣ  
-c n,��????oncurrent=n ģ����n���û���ͬʱ����,n��Ҫ���̫��,��ΪԽ��,siege ���ı��ػ�������ԴԽ��  
-i,????nternet �������urls.txt�е�url�б���,�Դ�ģ����ʵ�ķ������(�����),��urls.txt��������Ч  
-d n,????elay=n hitÿ��url֮����ӳ�,��0-n֮��  
-r n,????eps=n �ظ����в���n��,������ -tͬʱ����  
-t n,????ime=n ��������siege ��n����(��10S),����(10M),Сʱ(10H)  
-l ���н���,��ͳ�����ݱ��浽��־�ļ���siege .log,һ��λ��/usr/local/var/siege .log��,Ҳ����.siegerc���Զ���  
-R SIEGERC,????c=SIEGERC ָ�����ض���siege �����ļ�������,Ĭ�ϵ�Ϊ$HOME/.siegerc  
-f FILE, ????ile=FILE ָ�����ض���urls�ļ�����siege ,Ĭ��Ϊurls.txt,λ��siege ��װĿ¼�µ�etc/urls.txt  
-u URL,????rl=URL ����ָ����һ��URL,�������С�siege ��,��ѡ�������й�urls�ļ����趨  

urls.txt�ļ����Ǻܶ��д�����URL���б��Ի��з��Ͽ�,��ʽΪ:  
[protocol://]host.domain.com[:port][path/to/file]  


```
Transactions:		          30 hits        ## ��ɴ�����30
Availability:		      100.00 %           ## ���ã��ɹ���100%
Elapsed time:		        4.67 secs        ## ��ʱ4.67��
Data transferred:	        0.07 MB          ## ���ݴ���0.07MB
Response time:		        0.50 secs        ## ��Ӧʱ��0.50��
Transaction rate:	        6.42 trans/sec   ## ÿ�����6.42������
Throughput:		        0.01 MB/sec          ## ��������ÿ�봫��0.01MB
Concurrency:		        3.21             ## ʵ����߲���������
Successful transactions:          30         ## �ɹ���ɴ���30��
Failed transactions:	           0         ## ʧ��0��
Longest transaction:	        2.25         ## ÿ�δ��������ʱ��
Shortest transaction:	        0.37         ## ÿ�δ����������ʱ��
```
```
Transactions: siege�Է������ķ��ʴ��������ҳ�淢����redirect����ôsiege�Ὣ��ת���������������һ��transaction
Availability: socket���ӵĳɹ��ʡ��㷨�ǣ����ҳ�淢����timeout,4xx,5xx����ô����������ʧ�����󣬳ɹ��ʾ͵���(��������-ʧ������) / ��������
Elapsed time: ��������ķѵ�ʱ��
Data transferred: ����������������������������headers��content�����������ֵ���ܱ�server��ͳ�Ƶ���ֵҪ��һ��
Response time: ƽ����Ӧʱ��
Transaction rate: Transactions / Elapsed time
Throughput: ÿ��ƽ�������������
Concurrency: ƽ��������������
Successful transactions: ����status code < 400��transactions����
Failed transactions: ����status code >= 400��transactions����
Longest transaction: ���ʱ������ʱ��
Shortest transaction: ��̵�������ʱ��
```



����:
ѹ�Ⲣ��5�ˣ��ظ�����
```
siege -c5 -r2 http://www.bing.com
```
�ڴ˻��������ӳ���ʱ�䣬����Ϊ5��

```
siege -c5 -r2 -t5S http://www.bing.com
```

siege֧��https
```
sudo apt-get install openssl
sudo apt-get install libssl-dev
```
�����װʧ�ܣ���Ҫ������������  
Could not get lock /var/lib/dbkg/lock
```
sudo mv /var/lib/dpkg/info /var/lib/dpkg/info.bak
sudo mkdir /var/lib/dpkg/info
sudo apt-get update
```
```
./configure -with-ssl=./configure --with-ssl
sudo make
sudo make clean
sudo make install
```
�ڰ�װǰ��Ҫmack clean,����https����Ч���������������ҳ  
https://stackoverflow.com/questions/42367606/siege-https-error-https-requires-libssl



