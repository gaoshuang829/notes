���vim������������⣺  
��vim�������ļ���λ���� /etc/vim/vimrc �����м���  

```
set fileencodings=utf-8,gb2312,gbk,gb18030  
set termencoding=utf-8  
set encoding=prc  
```
�����˳�



����gedit������������£�
���ն������� gconf-editor 
�ڴ򿪵Ľ�����ѡ�� apps->gedit-2->preferences->encodings 
���ұߵ� auto_detected �� shown_in_menu �ϵ��Ҽ��༭���� add���ֱ����GB2312(������GB18030��,���� UP��ť�ƶ�����һλ���رգ��Ϳ�����gedit����ʾ������.

github  
1/Ϊ����github�ܹ�ʶ���������Լ��ϴ��ļ�����Ҫ����ssh key  
```
ssh-keygen -t rsa -C "your_email@youremail.com"
```

2/�����ñ��ص�ssh key��,�����ɵ�ssh key���Ƴ�����д��github�����ն�����
```
cat ~/.ssh/id_rsa.pub
```

�ն˻���ʾ���ոմ����õ�ssh key�����Ƴ�������github�ڵ��ͷ��Ȼ����setting�����ҵ�SSH and GPG keys������һ��new ssh key��Ȼ�󽫸ոո��Ƶ�ssh key���뼴�ɡ�

3/������ͨ��
```
ssh -T git@github.com
```

4/����commit��username��email��github���¼  
```
git config --global user.name "your name"
git config --global user.email "your_email@youremail.com"
```
5/���Զ�ֿ̲��ַ,yourName��yourRepo�ֱ������github���û����Ͳֿ�����
```
git remote add origin git@github.com:yourName/yourRepo.git
```


