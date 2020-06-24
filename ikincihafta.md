##6 Haziran##

**Github'ın Gitflow'u ile diğer yaklaşımları arasındaki fark nedir? ( gitflow vs...)**

Git flow'un birçok örneği bulunmaktadır:

**-GitFlow**

- [x] Feature/topic branches kullanımı
- [x] Release branches kullanımı
- [ ] Rebasing
- Merges: Hızlı olmayan merge işlemi.

![Gitflow](https://iamchuka.com/content/images/2018/05/gitflowimage.png)

**-GitHub Flow**
- [x] Feature/topic branches kullanımı
- [ ] Release branches kullanımı
- [ ] Rebasing
- Merges: Üstü örtük merging stratejisi

![Github Flow](https://user-images.githubusercontent.com/6351798/48032310-63842400-e114-11e8-8db0-06dc0504dcb5.png)

**-OneFlow**
- [x] Feature/topic branches kullanımı
- [x] Release branches kullanımı
- Rebasing: Opsiyonel
- Merges: Kişinin tercihine bağlı

![OneFlow](https://www.endoflineblog.com/img/oneflow/hotfix-branch-merge-final.png)

**-GitLab Flow**
- [x] Feature/topic branches: Yes.
- [x] Release branches: Yes.
- Rebasing: Opsiyonel
- Merges: Kişinin tercihine bağlı
- Other: Integrates with issue-tracking. Use of “environment” branches.

![GitLab Flow](https://miro.medium.com/max/1194/1*Kva1lwE4KCT_fdc6yHeGKQ.png)

[Kaynak:War of the Git Flows](https://dev.to/scottshipp/war-of-the-git-flows-3ec2)



**Git and GitHub with Briana Swift Youtube Listesi incelensin. (11 Video)**

1.[Github Workflow](https://www.youtube.com/watch?v=47E-jcuQz5c&list=PLg7s6cbtAD17Gw5u8644bgKhgRLiJXdX4&index=1)

2.[Working Locally](https://www.youtube.com/watch?v=rBbbOouhI-s&list=PLg7s6cbtAD17Gw5u8644bgKhgRLiJXdX4&index=2)

3.[Git Status](https://www.youtube.com/watch?v=rBbbOouhI-s&list=PLg7s6cbtAD17Gw5u8644bgKhgRLiJXdX4&index=3)

4.[Saved Changes](https://www.youtube.com/watch?v=rBbbOouhI-s&list=PLg7s6cbtAD17Gw5u8644bgKhgRLiJXdX4&index=4)

5.[Git Pull & Git Push](https://www.youtube.com/watch?v=rBbbOouhI-s&list=PLg7s6cbtAD17Gw5u8644bgKhgRLiJXdX4&index=5)

6.[Git Reset](https://www.youtube.com/watch?v=rBbbOouhI-s&list=PLg7s6cbtAD17Gw5u8644bgKhgRLiJXdX4&index=6)

7.[Merge Strategies](https://www.youtube.com/watch?v=rBbbOouhI-s&list=PLg7s6cbtAD17Gw5u8644bgKhgRLiJXdX4&index=7)

8.[Organization & Teams](https://www.youtube.com/watch?v=rBbbOouhI-s&list=PLg7s6cbtAD17Gw5u8644bgKhgRLiJXdX4&index=8)

9.[Migrate to Github](https://www.youtube.com/watch?v=rBbbOouhI-s&list=PLg7s6cbtAD17Gw5u8644bgKhgRLiJXdX4&index=9)

10.[Integrations](https://www.youtube.com/watch?v=rBbbOouhI-s&list=PLg7s6cbtAD17Gw5u8644bgKhgRLiJXdX4&index=10)

11[Changing History](https://www.youtube.com/watch?v=rBbbOouhI-s&list=PLg7s6cbtAD17Gw5u8644bgKhgRLiJXdX4&index=11)

**Merge pull request**
 
 **-Create a merge commit**
 
 "When you click the default Merge pull request option on a pull request on GitHub, all commits from the feature branch are added to the base branch in a merge commit."
 
 *(Github'daki pull request'lerden olan ve varsayılan olarak gelen Merge pull request'e tıkladığınızda, yan branchlerden gelen commitler temel branch olan merge commit'e eklenir.)*
 
 ![Merge Commit](https://help.github.com/assets/images/help/pull_requests/standard-merge-commit-diagram.png)
 
 **Squash and merge**
 
"When you select the Squash and merge option on a pull request on GitHub, the pull request's commits are squashed into a single commit. Instead of seeing all of a contributor's individual commits from a topic branch, the commits are combined into one commit and merged into the default branch."
 
"You can use squash and merge to create a more streamlined Git history in your repository. Work-in-progress commits are helpful when working on a feature branch, but they aren’t necessarily important to retain in the Git history. If you squash these commits into one commit while merging to the default branch, you can retain the original changes with a clear Git history."

*Squash and merge seçeneğini tıkladığınızda, pull request commitleri bir commit içinde toplanır. Tüm katkı sunanların tek tek commitlerini görmek yerine tüm commitler bir committe toplanır ve varsayılan branch ile merge edilir. Squash ve merge seçeneğini repositoryde daha derli toplu bir Git geçmişi yaratmak için kullanabilirsiniz. Bir yan branch üzerinde çalışırken süreci gösteren commitler yararlı olabilir ama Git geçmişinde tutmak çok da ihtiyaç dahilinde olmayabilir. Eğer varsayılan branch'e merge işlemi yaparken commitleri tek bir commite squash ediyorsanız, orijinal değişiklikleri temiz bir Git geçmişi ile birlikte bulundurmak isteyebilirsiniz.*
 
![](https://help.github.com/assets/images/help/pull_requests/commit-squashing-diagram.png)
 
**Rebase and merge**

When you select the Rebase and merge option on a pull request on GitHub, all commits from the topic branch (or head branch) are added onto the base branch individually without a merge commit. Pull requests with rebased commits are merged using the fast-forward option.

To rebase and merge pull requests, you must have write permissions in the repository, and the repository must allow rebase merging.
 
*Github'ta pull request yaparken Rebase and merge seçeneğine tıklarsanız, topic branchteki(ya da head branch'teki) tüm commitler bireysel olarak merge commit olmadan base branch'e eklenir. Rebased commitli pull requestler [fast-forward](https://git-scm.com/docs/git-merge#_fast_forward_merge) seçeneği ile merge edilerek kullanılır.*

*Rebase ve merge pull request için repository'e yazma izninizin olması gerekir ve repository rebase merging'e izin vermelidir.*

[Kaynak:Github](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-request-merges)

 **issue ve #pull request de id ler neden artıyor farklı sekmeler olmasına rağmen?**
 
 
 
 **Ramp up on Git and GitHub**
 
- [X] Kursa başlangıç yapıldı.
 
 
 **Aspnetboilerplate ve yan ürünler araştırması. AspNet Boilerplate - Web Application Framework**
 
"ASP.NET Boilerplate is a general purpose application framework especially designed for new modern web applications. It uses already familiar tools and implements best practices around them to provide you a SOLID development experience."

(ASP.NET Boilerplate genel amaçlı bir uygulama frameworküdür. Özellikle yeni modern web uygulamaları için tasarlanmıştır. Halihazırda benzer araçları kullanıp size SOLID geliştirme deneyimi sunmak için best practisleri uygular.)

- Domain Driven Design(DDD) temeli üzerinde katmanlı mimari olanağı sağlar.
- Database'den UI'a kadar multitenancy ile uyumlu.
- Modüler olarak tasarlanmıştır.

[Kaynak: ASP.NET Boilerplate](https://aspnetboilerplate.com/)
 
 
 **hackerRank.com --> 30 Days Of Code**
 
 - [X] Başlangıç yapıldı(6/30).
 
 
 ##7 Haziran Ödevleri
 
 
**Razor Pages Nedir?**
 
** 4 Farklı Projede Yapılacak Change Authentication**
 
 -[No Authentication](https://github.com/Kodluyoruz51BootcampMVCCore/arastirma-odevi-omrfyildiz/tree/master/Authentications/No_Authentication)
 
 -[Individual User Account](https://github.com/Kodluyoruz51BootcampMVCCore/arastirma-odevi-omrfyildiz/tree/master/Authentications/Individual%20User%20Account)
 
 -[Work or School Accounts](https://github.com/Kodluyoruz51BootcampMVCCore/arastirma-odevi-omrfyildiz/tree/master/Authentications/Work%20or%20School%20Accounts)
 
 -Windows Authentication seçili projeler oluşturulmalı
 
 
 **Ayarlardaki Output kısmındaki Console Application nedir? diğerleri arasında fark nedir?**

Bir Console Application(Uygulaması), C# bağlamında düşünürsek, üç temel data akışına(standart input, standart output ve standart error) erişerek girdileri alıp çıktıları gösteren bir komut satırı(command line) konsol uygulamasıdır. Bir konsol uygulaması genellikle stand-alone executable dosya formatı içinde ya minimal bir grafik arayüzü barındırır ya da hiç barındırmaz.

[Kaynak: Technopedia](https://www.techopedia.com/definition/25593/console-application-c)
 
 **c# json serialize / deserialize**
 
 **Serialization:** Bir nesnedeki verinin bir yerde depolaması veya ağ ortamında bir yerden bir yere gönderilmesi gerektiği durumlarda uygun formata dönüştürülmesi işlemine serileştirme denir. Serileştirilen nesneler veritabanı, hafıza veya dosya gibi ortamlarda saklanabilirler. [Kaynak](https://www.bayramucuncu.com/c-ile-serilestirme-serialization/)
 
 **Deserialisation:** Ulaşılabilir hale gelmiş datayı tekrardan hangi dilde yazıyorsak o dildeki objeye çevirmektir.[Kaynak](https://medium.com/@emrebalcii94/messagepack-nedir-serialize-deserialize-y%C3%B6ntemleri-neden-%C3%B6nemlidir-836a5f85b7b8#:~:text=K%C4%B1saca%20bahsedecek%20olursak%20serialize%20ya,yaz%C4%B1yorsak%20o%20dildeki%20objeye%20%C3%A7evirmektir.)
 
 [**JSON Serialize and Deserialize on .NET**](https://docs.microsoft.com/tr-tr/dotnet/standard/serialization/system-text-json-how-to) 
 
 
 **MVC vs MVVM**
 
 **MVP vs MVW vs MVU Pattern arasındaki fark**
 
 ![Görsel](https://i.stack.imgur.com/Y82D3.png)
 
 [StackOverflow](https://stackoverflow.com/questions/19444431/what-is-difference-between-mvc-mvp-mvvm-design-pattern-in-terms-of-coding-c-s)
 
 [Microsoft](https://docs.microsoft.com/en-gb/archive/blogs/erwinvandervalk/the-difference-between-model-view-viewmodel-and-other-separated-presentation-patterns)
 
 **Model-View-Update (MVU) nedir?**
 
Kullanıcıya sunulan arayüzde(View) kullanıcının aldığı aksiyonun(Update) modelde yarattığı değişikliği ifade eder.
 
[Ayrıntılar için:](https://elmish.github.io/elmish/)
