[Сообщество](/README.RU.md) | [Все мероприятия](/Events.RU.md) | [База знаний](/KB/README.RU.md)

# PPML (Privacy Preserving ML)

На самом деле Not only PP и Not only ML: раздел посвящён вопросам безопасного объединения данных различных организаций для их совместного анализа.

**Ключевые слова:** гомоморфное шифрование (FHE, PHE, SHE), cовместные конфиденциальные вычисления (SMPC), доверенные среды исполнения (TEE), криптоанклавы, федеративное обучение (FL), дифференциальная приватность, синтетические данные с сохранение структурных связей, внешние данные, обогащение данных, коллаборация данных.

**Содержание**

* [Все мероприятия сообщества по теме](#все-мероприятия-сообщества-по-теме)
* [Конфиденциальная аналитика: с чего начать?](#конфиденциальная-аналитика-с-чего-начать)
* [Материалы для более глубокого изучения](#материалы-для-более-глубокого-изучения):
    * [Общее](#общее)
    * [Гомоморфное шифрование](#гомоморфное-шифрование)
    * [Криптоаклавы](#криптоанклавы)
    * [Дифференциальная приватность](#дифференциальная-приватность)
    * [Федеративное обучение](#федеративное-обучение)
    * [Синтетические данные](#синтетические-данные)
* [Ландшафты решений](#ландшафты-решений)
    * [Криптоанклавы (2023)](#криптоанклавы-2023)
    * [Федеративное обучение (2023)](#federated-learning-2023)
    * [Синтетические данные (2023)](#синтетические-данные-2023)
* [Полезные ресурсы](#полезные-ресурсы)

## Все мероприятия сообщества по теме

* СОЗВОН: Дмитрий Маслов, Михаил Фатюхин, Денис Афанасьев, Евгений Попов, Роман Постников, Павел Снурницын, Federated Learning и конфиденциальный анализ данных. [YouTube](https://youtu.be/JpApLfde38I) \| [Дзен](https://dzen.ru/video/watch/6820f8ad299a2d186a9f0b8b) \| [RuTube](https://rutube.ru/video/4feeead3035a80bc8d3bc405d281fab3/) *(~1 час 25 минут)*;

* Евгений Попов, Никита Лазарев, Юрий Маркин, Практический опыт применения FL в медицине на примере обучения модели по классификации ЭКГ-синдромов, 2024. [YouTube](https://youtu.be/lACZk15hUb8) | [Дзен](https://dzen.ru/video/watch/66d0a1e348695e3387dccfea) | [RuTube](https://rutube.ru/video/f15475d79a95c07611f946825c432690/) *(~1 час 35 минут)*;

* Денис Афанасьев, Федеративное обучение: обзор методов, платформ и трендов, 2024. [YouTube](https://youtu.be/eD3KngY_tM8) | [Дзен](https://dzen.ru/video/watch/669b7506eb82615474b94cbe) | [RuTube](https://rutube.ru/video/8f841f1db5cd25fa61aeba01e7ceb516/) *(~1 час 20 минут)*;

* Роман Постников, Максим Воеводский, Upgini: Библиотека для поиска и обогащения ML моделей релевантными внешними фичами, 2023. [YouTube](https://youtu.be/-KuvxJXJDqk) | [Дзен](https://dzen.ru/video/watch/66d0a116cfdd4f4c6c75446d) | [RuTube](https://rutube.ru/video/976c3846cfb6ca4672b8c8f29640fea5/) *(~1 час 25 минут)*

* СОЗВОН: Роман Постников, Павел Снурницын, Александр Григорьевский, Андрей Соколов, Методы конфиденциальной аналитики, 2023. [YouTube](https://youtu.be/lACZk15hUb8) | [Дзен](https://dzen.ru/video/watch/66d0a1e348695e3387dccfea) | [RuTube](https://rutube.ru/video/f15475d79a95c07611f946825c432690/) *(~1 час 50 минут)*;

* Денис Афанасьев, Таксономия методов FL, обзор платформ, основных игроков, вызовов и трендов развития, 2023. [YouTube](https://youtu.be/g14cVjUxNlE) | [Дзен](https://dzen.ru/video/watch/66d09fa6a6fec84560d347e2) | [RuTube](https://rutube.ru/video/42f7336b7675cf0d4b022129f40ca6bd/) *(~1 час 20 минут)*;

* Фёдор Смирнов, Гузелия Мошнина, Рахмет Оджаев, Методы генерации синтетических данных, 2023. [YouTube](https://youtu.be/PxZhfVx2k0E) | [Дзен](https://dzen.ru/video/watch/66d0a5f037081c7ef1978be6) | [RuTube](https://rutube.ru/video/4e1c01241db064d7b45b104c906b5523/) *(~1 час 40 минут)*;

* ПОДКАСТ: Лев Рагулин, Конфиденциальные и совместные вычисления на основе ML, 2022. [YouTube](https://youtu.be/bPhRArMr-ac) | [Дзен](https://dzen.ru/video/watch/66d0a673fc532104b3e9671f) | [RuTube](https://rutube.ru/video/6cee1d553434d617412b5aee3ca86be7/) *(~35 минут)*.

## Конфиденциальная аналитика: с чего начать?

**Общее**

У нас сложилась такая верхнеуровневая классификация методов PPML:
* Гомоморфное шифрование (FHE, SHE, PHE);
* Совместные конфиденциальные вычисления (SMPC);
* Криптоанклавы (доверенные среды исполнения, TEE);
* Федеративное обучение (FL);
* Дифференциальная приватность;
* Cинтетические данные (с сохранение структурных связей и зависимостей);

Материалы организованы согласно этой классификации (хотя перечисленные методы часто взаимно дополняют друг друга).

Краткие обзоры:
* [Why confidential computing will be critical to (not so distant) future data security efforts](https://venturebeat.com/security/why-confidential-computing-will-be-critical-to-not-so-distant-future-data-security-efforts/), 2023 *(~6 минут)*.
* [Get Ready For Confidential Computing](https://gradientflow.com/get-ready-for-confidential-computing/), 2021, и продолжение [Confidential Computing and Machine Learning](https://gradientflow.com/confidential-computing-and-machine-learning/), 2022 *(~10 минут)*.
* [Privacy-Enhancing Technologies (PETs): An adoption guide (Palantir RFx Blog Series)](https://blog.palantir.com/privacy-enhancing-technologies-pets-an-adoption-guide-palantir-rfx-blog-series-6-b02dad56e9da), 2023 *(~14 минут)*.
* Доклад: [Павел Снурницын, Конфиденциальная аналитика или Анализ данных без данных](https://rutube.ru/video/461da4a7691b456d9de9a20d10f9ab94/?r=wd&t=6616), 2024 *(~15 минут)*. 

Отчёт АБД:
* [Технологии защищенной обработки данных: от защиты данных — к развитию ИИ, партнерским отношениям и экосистемной экономике](https://lib.rubda.ru/public/tekhnologii-zashchishchennoj-obrabotki-dannyh1.html), 2024 *(~30 минут)*;

Более детальное введение:
* [Privacy Enhancing Technologies: An Introduction for Technologists](https://martinfowler.com/articles/intro-pet.html), 2023 *(30 минут)*.

Про текуще положение дел:
* [Мысли про FL и PPML по мотивам созвона](../2025/2025-05-07-CALL-FL/README.md#мысли-про-fl-и-ppml-по-мотивам-созвона), 2025 *(~2 минуты)*.

**Гомоморфное шифрование**

Вводное:
* [What is Homomorphic Encryption?](https://blog.openmined.org/what-is-homomorphic-encryption/) (С примерами на PySyft), 2020 (15 минут);
*  Доклад на fhe.org: [Pascal Paillier - Introduction to Homomorphic Encryption](https://youtu.be/umqz7kKWxyw), 2020 (1 час).

Несколько конкретных примеров из блога Zama:
* [Linear Regression Over Encrypted Data With Homomorphic Encryption](https://www.zama.ai/post/linear-regression-using-linear-svr-and-concrete-ml-homomorphic-encryption), 2023;
* [How to Deploy a Machine Learning Model With Concrete ML](https://www.zama.ai/post/how-to-deploy-machine-learning-models-with-concrete-ml), 2023;
* [Video tutorial] [How To Convert a Scikit-learn Model Into Its Homomorphic Equivalent](https://www.zama.ai/post/how-to-convert-a-scikit-learn-model-into-its-homomorphic-equivalent), 2023.

**Совместные конфиденциальные вычисления**

Краткое введение:
* [Денис Афанасьев, Совместные конфиденциальные вычисления на пальцах](https://habr.com/ru/articles/660813/), 2022 *(~5 минут)*.

Отчёт АБД:
* [Конфиденциальные вычисления и доверенные среды исполнения. Secure Multiparty Computation](https://lib.rubda.ru/public/secure-multiparty-computation.html), 2025 *(~30 минут)*.

**Криптоанклавы**

Простые введения:
* [What Is Confidential Computing?](https://blogs.nvidia.com/blog/2023/03/01/what-is-confidential-computing/) 2023 *(~7 минут)*;
* [Verifiably Private Computation](https://brave.com/verifiably-private-computation/) (есть на [русском](https://habr.com/ru/companies/brave/articles/717916/)), 2023 *(~5 минут)*.

Статьи oneFactor про кейс на Intel SGX:
* [Как в oneFactor ускорили безопасное обучение ML-алгоритмов в 19 раз с помощью Intel Xeon Gen3 и SGX 2.0](https://habr.com/en/company/intel/blog/560598/), 2021 (4 минуты);
* [Задача конфиденциальности данных поставщика](https://medium.com/onefactor-russia/%D0%B7%D0%B0%D0%B4%D0%B0%D1%87%D0%B0-%D0%BA%D0%BE%D0%BD%D1%84%D0%B8%D0%B4%D0%B5%D0%BD%D1%86%D0%B8%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D1%81%D1%82%D0%B8-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85-%D0%BF%D0%BE%D1%81%D1%82%D0%B0%D0%B2%D1%89%D0%B8%D0%BA%D0%B0-aecfdadd3d1f), 2021 (3 минуты).

Отчёт АБД:
* [Конфиденциальные вычисления и доверенные среды исполнения](https://lib.rubda.ru/public/tekhnologii-zashchishchennoj-obrabotki-dannyh2.html), 2024 *(~30 минут)*.

**Дифференциальная приватность**

Две хорошие вводные серии постов и доклад. Чтобы понять в чем суть, можно почитать пару первых статей из каждой серии, займет 10-15 минут:
* [Differential Privacy Blog Series](https://www.nist.gov/itl/applied-cybersecurity/privacy-engineering/collaboration-space/focus-areas/de-id/dp-blog) (есть переводы первых двух статей [тут](https://habr.com/ru/companies/domclick/articles/526724/) и [тут](https://habr.com/ru/companies/domclick/articles/527258/)), 2020-2022 *(~1 час 30 минут)*;
* [A friendly, non-technical introduction to differential privacy](https://desfontain.es/privacy/friendly-intro-to-differential-privacy.html), 2021-2023 *(~2 часа)*. Здесь отдельно хочется подсветить пост про кейсы: [A list of real-world uses of differential privacy](https://desfontain.es/privacy/real-world-differential-privacy.html);
* Доклад Синтии Дворк, одной из основоположников формальной дифференциальной приватности: [The Definition of Differential Privacy - Cynthia Dwork](https://youtu.be/lg-VhHlztqo), 2016 *(~20 минут)*.

**Федеративное обучение**

Два кратких вводных поста с текущим положением дел:
* [Евгений Попов, Что такое федеративное обучение: метод, который приведет к взрывному росту искусственного интеллекта](https://www.techinsider.ru/technologies/1677577-chto-takoe-federativnoe-obuchenie-metod-kotoryi-privedet-k-vzryvnomu-rostu-iskusstvennogo-intellekta/), 2025 *(~7 минут)*;
* [Денис Афанасьев, Федеративное обучение: потенциал, ограничения и экономические реалии внедрения](https://habr.com/ru/articles/909014/), 2025 *(~5 минут)*.

Отчёт АБД:
* [Конфиденциальные вычисления и доверенные среды исполнения. Federated Learning](https://lib.rubda.ru/public/fl-multiparty-computation.html), 2025 *(~30 минут)*.

**Синтетические данные сохраняющие структуру**

Рассуждения Gartner про захват мира синтетическими данными:
* [Is Synthetic Data the Future of AI?](https://www.gartner.com/en/newsroom/press-releases/2022-06-22-is-synthetic-data-the-future-of-ai), 2022 *(~3 минуты)*;
* [Can synthetic data drive the future of AI?](https://aibusiness.com/data/gartner-can-synthetic-data-drive-the-future-of-ai-), 2022 *(~3 минуты)*.

Верхнеуровневые кейсы и ландшафт инструментов:
* [Synthetic data is the future of Artificial Intelligence](https://moez-62905.medium.com/synthetic-data-is-the-future-of-artificial-intelligence-6fcfd2ce1a14), 2023 *(~12 минут)*;

Избранное из блога Gretel:
* Про кейс, как синтетические данные помогут обезопасить работу с чувствительными данными при привлечении консультантов для построения моделей: [How to safely work with another company's data](https://gretel.ai/blog/how-to-safely-work-with-another-companys-data), 2022 *(~5 минут)*;
* На одном из семинаров поднимался вопрос про синтетический кликстрим, который мы свели к генерации последовательностей, а тут пример генерации временного ряда: [Generate time-series data with Gretel’s new DGAN model](https://gretel.ai/blog/generate-time-series-data-with-gretels-new-dgan-model), 2022 *(~6 минут)*;
* Про встраивание в ландшафт MLOps: [Synthetic Data and the Data-centric Machine Learning Life Cycle](https://gretel.ai/blog/synthetic-data-and-the-data-centric-machine-learning-life-cycle), 2022 *(~5 минут)*;
* Подкаст, про синтетику в целом, и есть пара интересных историй про реальные кейсы использования: [Graymatter - Making Data Work](https://gretel.ai/podcasts/making-data-work), 2022 *(~35 минут)*.

## Материалы для более глубокого изучения

### Общее

Курсы:
* Вводный и очень неспешный курс: [OpenMined Foundations of Private Computation](https://courses.openmined.org/courses/foundations-of-private-computation);
* Курс на Udacity от OpenMined: [Secure and Private AI](https://www.udacity.com/course/secure-and-private-ai--ud185). 

Книги:
* [J.M. Chang, Di Zhuang,  G.D. Samaraweera - Privacy-Preserving Machine Learning](https://www.manning.com/books/privacy-preserving-machine-learning), 2023. Здесь фокус в основном на дифференциальную приватность, есть про синтетику и немного про FHE.
* [K. Jarmul - Practical Data Privacy](https://www.oreilly.com/library/view/practical-data-privacy/9781098129453/), 2023. Здесь по содержанию выглядит, что дано более полное покрытие области.

### Гомоморфное шифрование

Избранные научные публикации:
* [I. Chillotti et al., TFHE: Fast Fully Homomorphic Encryption over the Torus](https://eprint.iacr.org/2018/421), 2018.
    * Плюс сопроводительная серия постов: [TFHE Deep Dive](https://www.zama.ai/post/tfhe-deep-dive-part-1), 2022 *(~1,5 часа)*;
    * И доклад на fhe.org: [Ilaria Chillotti - TFHE Deep Dive](https://youtu.be/npoHSR6-oRw), 2021 *(~2 часа)*.
* [A. Benamira et al., TT-TFHE: a Torus Fully Homomorphic Encryption-Friendly Neural Network Architecture](https://arxiv.org/abs/2302.01584), 2023.
    * Доклад на fhe.org: [Adrien Benamira - TT-TFHE: Torus FHE-Friendly Neural Network Architecture](https://youtu.be/_yvYHipEByI), 2023 *(~45 минут)*.
* См. также список [Influential Papers на FHE.org](https://fhe.org/resources/#influential-papers)

### Криптоанклавы

Избранные научные публикации:
* Отличная статья с обзором текущего положения дел в области приложения TEE к ML: [F. Mo, Z. Tarkhani, H. Haddadi - Machine Learning with Confidential Computing: A Systematization of Knowledge](https://arxiv.org/abs/2208.10134), 2022.

### Дифференциальная приватность

Книга:
* [Cynthia Dwork, Aaron Roth, The Algorithmic Foundations of Differential Privacy](https://www.cis.upenn.edu/~aaroth/privacybook.html), 2014.

### Федеративное обучение

Книги:
* [D.C. Verma, Federated AI for Real-World Business Scenarios](https://www.amazon.com/Federated-AI-Real-World-Business-Scenarios-ebook/dp/B099F6VG2Q), 2021.
Книга ориентирована на бизнес аналитиков и архитекторов, фокус больше на кейсы Enterprise FL (в противопоставление Consumer FL, то есть FL на мобильных устройствах). Получился достаточно хороший обзор темы с точки зрения поиска применений в бизнесе.
* [K. Nakayama, G. Jeno, Federated Learning with Python](https://www.packtpub.com/product/federated-learning-with-python/9781803247106), 2022.
Это уже учебник с примерами кода и дизайн паттернами FL.

Сборники статей:
* [Federated Learning: A Comprehensive Overview of Methods and Applications](https://ibmfl.mybluemix.net/Book), 2022.
* [Federated Learning for IoT Applications](https://link.springer.com/book/10.1007/978-3-030-85559-8), 2022.

Избранные научные публикации:
* [F. Liu et al., A survey on federated learning: a perspective from multi-party computation](https://link.springer.com/article/10.1007/s11704-023-3282-7), 2023. Короткий и относительно свежий обзор методов и работ по конфиденциальности в FL: и HE, и дифференциальная приватность, и SMPC, плюс явные акценты и комментарии на задачи оптимизации точности моделей и производительность схем обеспечения конфиденциальности.
* [Y.Zhang et al., A Survey of Trustworthy Federated Learning with Perspectives on Security, Robustness, and Privacy](https://arxiv.org/abs/2302.10637), 2023. Здесь еще более широкий контекст доверенного (или доверительного) FL, более четко определяются границы конфиденциальности и безопасности, а еще есть про робастность получаемых моделей.
* [L. Yuan et al., Decentralized Federated Learning: A Survey and Perspective](https://arxiv.org/abs/2306.01603), 2023.
* [A. El Ouadrhiri, Differential Privacy for Deep and Federated Learning: A Survey](https://www.researchgate.net/publication/359005353_Differential_Privacy_for_Deep_and_Federated_Learning_A_Survey), 2022.

### Синтетические данные

Книги:
* [K. El Emam, L. Mosquera, R. Hoptroff, Practical Synthetic Data Generation](https://www.oreilly.com/library/view/practical-synthetic-data/9781492072737/), 2020;
* [V. Granville, eBook: Synthetic Data and Generative AI, with Applications](https://mltechniques.com/product/ebook-synthetic-data/), v3.0, 2023. 


Избранные научные публикации:
* Статья про CTGAN: [L. Xu, M. Skoularidou, Al. Cuesta-Infante, K. Veeramachaneni - Modeling Tabular data using Conditional GAN](https://arxiv.org/abs/1907.00503), 2019.
* Байесовские сети для генерации синтетики: [I. Deeva, A. Mossyayev, A.V. Kalyuzhnaya - A Multimodal Approach to Synthetic Personal Data Generation with Mixed Modelling: Bayesian Networks, GAN’s and Classification Models](https://www.researchgate.net/publication/358456183_A_Multimodal_Approach_to_Synthetic_Personal_Data_Generation_with_Mixed_Modelling_Bayesian_Networks_GAN%27s_and_Classification_Models), 2022.

## Ландшафты решений

Ландшафты открытых и коммерческих решений по основным подходам PPML, в скобках указан год составления/актуализации ландшафта.

### Криптоанклавы (2023)

* Intel SGX
* AMD SEV
* ARM TrustZone
* [AWS Nitro Enclaves](https://aws.amazon.com/ec2/nitro/nitro-enclaves/)
* [NVIDIA Confidential Computing](https://www.nvidia.com/en-us/data-center/solutions/confidential-computing/)

### Federated Learning (2023)

**Открытие фреймворки и библиотеки** (в скобках указан основной контрибьютер, если есть):
* [TensorFlow Federated](https://www.tensorflow.org/federated/get_started) (Google);
* [FLUTE](https://github.com/microsoft/msrflute) (Microsoft);
* [OpenFL](https://github.com/securefederatedai/openfl) (Intel);
* [FLARE](https://github.com/NVIDIA/NVFlare) (NVIDIA);
* [Crypten](https://github.com/facebookresearch/CrypTen) (Meta);
* [PySyft](https://github.com/OpenMined/PySyft) (OpenMined);
* [PaddleFL](https://github.com/PaddlePaddle/PaddleFL) (PaddlePaddle);
* [Fedlearner](https://github.com/bytedance/fedlearner) (ByteDance / TikTok);
* [FederatedScope](https://github.com/alibaba/FederatedScope) (Alibaba);
* [FEDn](https://github.com/scaleoutsystems/fedn) (Scaleout Systems);
* [Flower](https://github.com/adap/flower) (Flower);
* [FedML](https://github.com/FedML-AI) (FedML);
* [Substra](https://docs.substra.org/en/stable/) (Owkin);
* [FATE](https://github.com/FederatedAI/FATE) (FedAI / WeBank);
* [EasyFL](https://github.com/EasyFL-AI/EasyFL);
* [Plato](https://github.com/TL-System/plato);
* [Fed-DART](https://github.com/cc-hpc-itwm/Fed-DART);
* [FedTorch](https://github.com/MLOPTPSU/FedTorch);
* *[federated-learning-lib](https://github.com/IBM/federated-learning-lib) (IBM, не open source, открытая лицензия только для некоммерческого использования);
* *[Angel](https://github.com/Angel-ML/angel) (Tencent, Peking University) - фреймворк для распределенного ML, на базе которого есть некий Angel PowerFL, открытость которого не понятна.

Список открытых фреймворков есть еще тут: [Awesome Federated Machine Learning](https://github.com/innovation-cat/Awesome-Federated-Machine-Learning#open-sources), вместе с большим количеством литературы и другой полезной информации по теме.

UPD 2024:
* Stalactite — опенсорс фреймворк для VFL от ИТМО и Сбера: [GitHub](https://github.com/sb-ai-lab/Stalactite), [пресс-релиз](https://news.itmo.ru/ru/startups_and_business/partnership/news/13991/) и материалы конференции ACM RecSys ’24: [A. Zakharova et al., Stalactite: toolbox for fast prototyping of vertical federated learning systems](https://dl.acm.org/doi/abs/10.1145/3640457.3691700), 2024 *(~10-20 минут)*.

**Коммерческие платформы**

Во-первых, решения и сервисы, которые концентрируются на FL или даже немного шире, FL с применением других методов конфиденциальных вычислений:
* [integrate.ai](https://www.integrate.ai/);
* [sherpa.ai](https://www.sherpa.ai/);
* [Devron](https://www.devron.ai/);
* [Ichnite](https://intellegens.com/products-services/ichnite/);
* [Apheris](https://www.apheris.com/);
* [Databloom](https://www.databloom.ai/);
* [DynamoFL](https://www.dynamofl.com/);
* [YunFL](https://www.points.org/en/fl.html);
* [Adap](https://www.adap.com/en).

Во-вторых, полноценные DS/ML/MLOps платформы, в которых функционалу FL уделяется много внимания:
* [IBM Federated Learning](https://ibmfl.mybluemix.net/);
* [Scaleout Systems](https://www.scaleoutsystems.com/);
* [FeatureCloud](https://featurecloud.eu/);
* [Bitfount](https://www.bitfount.com/);
* [T-DAB.AI](https://t-dab.ai/).

В-третьих, направление FL плотно пересекается с безопасными анклавами и Data Clean Rooms, тут стоит подсветить:
* [Intel SGX](https://www.intel.com/content/www/us/en/developer/tools/software-guard-extensions/overview.html);
* [AWS Clean Rooms](https://aws.amazon.com/clean-rooms/).

Но технологии TEE/Secure Enclave и игроки Data Clean Rooms заслуживают отдельного более полного обзора.

На текущий момент больше всего кейсов применения FL концентрируется вокруг медицины и здравоохранения, тут есть отдельная ниша:
* [NVIDIA Clara](https://developer.nvidia.com/industries/healthcare);
* [Owkin](https://owkin.com/);
* [Rhino Health](https://www.rhinohealth.com/);
* [Clinerion](https://www.clinerion.com/index.html);
* [CERN CAFEIN](https://knowledgetransfer.web.cern.ch/kt-fund/projects/cafein-federated-network-platform-development-and-deployment-ai-based-analysis-and);
* [AI Centre FLIP](https://www.aicentre.co.uk/platforms#view2) (как раз на базе технологий TEE/Secure Enclave).

### Синтетические данные (2023)

Несколько обзоров инструментов для генерации синтетических данных:
* [15 Best Synthetic Data Generation Tools](https://squeezegrowth.com/synthetic-data-generation-tools/), 2023 *(~15 минут)*;
* [Top Synthetic Data Generation Tools](https://www.qwak.com/post/top-synthetic-data-generation-tools), 2023 *(~15 минут)*;
* [Synthetic data tools: Open source or commercial? A guide to building vs. buying](https://www.statice.ai/post/synthetic-data-open-source-tools-guide-building-buying), 2022 *(~8 минут)*.

Итого, вендоры и стартапы вокруг генерации синтетических данных для использования в ML/AI и аналитике:
* [Hazy](https://hazy.com/)
* [Datomize](https://www.datomize.com/)
* [Tonic](https://www.tonic.ai/)
* [Mostly](https://mostly.ai/)
* [Synthesized](https://www.synthesized.io/)
* [Gretel Synthetics](https://gretel.ai/)
* [YData Synthesizer](https://ydata.ai/products/synthesizer)
* [Facteus Mimic](https://www.facteus.com/mimic)
* [Syntho](https://www.syntho.ai/)
* [Statice](https://www.statice.ai/)
* [GenRocket](https://www.genrocket.com/)
* [Sogeti Artificial Data Amplifier](https://www.sogeti.com/services/artificial-intelligence/artificial-data-amplifier/)
* [Boogie Data Synthesizer](https://boogiesoftware.com/datasynth/)
* [DataCebo](https://datacebo.com/)

Отдельным списком - открытые инструменты и библиотеки:
* [SDV](https://sdv.dev/)
* [Synthesized SDK](https://docs.synthesized.io/sdk/latest/user_guide/install)
* [DoppelGANger](https://github.com/fjxmlzn/DoppelGANger)
* [Twinify](https://github.com/DPBayes/twinify)
* [DataGene](https://github.com/firmai/datagene) - инструмент для анализа качества синтетических данных
* [GAN for synthetic time series data](https://github.com/stefan-jansen/synthetic-data-for-finance) - генерации данных временных рядов

Более нишевые подходы:
* Решения для медицинских данных: [MDClone](https://www.mdclone.com/), [Synthea](https://synthetichealth.github.io/synthea/).
* Решения вокруг CV: [Anyverse](https://anyverse.ai/), [Datagen](https://datagen.tech/), [Synthesis](https://synthesis.ai/), [Neurolabs](https://www.neurolabs.ai/), [Rendered](https://rendered.ai/), [Oneview](https://one-view.ai/), [CVEDIA](https://www.cvedia.com/products/what-is-synthetic-data).
* Пример применения в других задачах: [Synthetica Data](https://syntheticadata.com/) - решение вопросов качества данных, дополнения пропущенных данных и т.п.

А есть еще кейс генерации синтетики для задач тестирования баз данных и приложений, в этом случае нет потребности переносить смысл и зависимости внутри реальных данных в синтетический датасет, то есть речь скорее про dummy data, а не synthetic data. Список инструментов которые помогут в этом случае:
* [Synth](https://www.getsynth.com/)
* [Faker](https://github.com/joke2k/faker)
* [Mimesis](https://mimesis.name/en/master/)
* [Plait.py](https://github.com/plaitpy/plaitpy)
* [Pydbgen](https://github.com/tirthajyoti/pydbgen)
* [Synner](https://github.com/huda-lab/synner)
* [mirrorGen](https://github.com/DataResponsibly/MirrorDataGenerator)

## Полезные ресурсы

* [Библиотека методов конфиденциальной работы с данными от Ассоциации Больших Данных](https://lib.rubda.ru)
* [FHE.org community](https://fhe.org)
* [OpenMined.org](https://openmined.org)