1. ͨ��git init��������Ŀ¼���Git���Թ���Ĳֿ�
  ������git add����Git�����ļ���ӵ��ֿ�,����Ӷ���ļ�
  ������git commit [-m "˵��"] ����Git�����ļ��ύ���ֿ�

2.  git status�������������ʱ�����ղֿ⵱ǰ��״̬
  ���git status���������ļ����޸Ĺ�����git diff���Բ鿴�޸�����

3.  Git���������ڰ汾����ʷ֮�䴩��ʹ������git reset --hard commit_id
  ����ǰ����git log���Բ鿴�ύ��ʷ���Ա�ȷ��Ҫ���˵��ĸ��汾
  Ҫ�ط�δ������git reflog�鿴������ʷ���Ա�ȷ��Ҫ�ص�δ�����ĸ��汾

4. ����1����������˹�����ĳ���ļ������ݣ���ֱ�Ӷ������������޸�ʱ��������git checkout -- file
    ����2�����㲻�������˹�����ĳ���ļ������ݣ�����ӵ����ݴ���ʱ���붪���޸ģ�����������һ��������git reset HEAD <file>���ͻص��˳���1����       ����������1����
    ����git rm����ɾ��һ���ļ������һ���ļ��Ѿ����ύ���汾�⣬��ô����Զ���õ�����ɾ������ҪС�ģ�git checkout --fileֻ�ָܻ��ļ������°汾��    ��ᶪʧ���һ���ύ�����޸ĵ�����)

5.Ҫ����һ��Զ�̿⣬ʹ������git remote add origin git@server-name:path/repo-name.git
  ������ʹ������git push -u origin master��һ������master��֧����������
  �˺�ÿ�α����ύ��ֻҪ�б�Ҫ���Ϳ���ʹ������git push origin master���������޸�

6.Ҫ��¡һ���ֿ⣬���ȱ���֪���ֿ�ĵ�ַ��Ȼ��ʹ��git clone�����¡. Git֧�ֶ���Э�飬����https����ͨ��ssh֧�ֵ�ԭ��gitЭ���ٶ����

7.Git��������ʹ�÷�֧��

�鿴��֧��git branch

������֧��git branch <name>

�л���֧��git checkout <name>

����+�л���֧��git checkout -b <name>

�ϲ�ĳ��֧����ǰ��֧��git merge <name>

ɾ����֧��git branch -d <name>
Creating a new branch is quick & simple.