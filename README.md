<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AniMeda — Смотри Аниме в HD</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Подключение шрифта Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <!-- Иконки Lucide -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0b0c10;
        }
        .custom-blur {
            backdrop-filter: blur(12px);
        }
        /* Стилизация скроллбара */
        ::-webkit-scrollbar {
            width: 8px;
            height: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0b0c10;
        }
        ::-webkit-scrollbar-thumb {
            background: #1f2937;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #3b82f6;
        }
    </style>
</head>
<body class="text-gray-100 antialiased min-h-screen flex flex-col">

    <!-- НАВИГАЦИЯ -->
    <header class="fixed top-0 left-0 right-0 z-50 bg-[#0b0c10]/70 custom-blur border-b border-gray-800/50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
            <!-- Логотип -->
            <div class="flex items-center gap-2 cursor-pointer group">
                <div class="w-9 h-9 bg-gradient-to-tr from-purple-600 to-indigo-500 rounded-xl flex items-center justify-center shadow-lg shadow-indigo-500/20 group-hover:scale-105 transition-transform">
                    <i data-lucide="play" class="w-5 h-5 text-white fill-white ml-0.5"></i>
                </div>
                <span class="text-xl font-bold tracking-wider bg-gradient-to-r from-white to-gray-400 bg-clip-text text-transparent">ANI<span class="text-indigo-500">MEDA</span></span>
            </div>

            <!-- Меню -->
            <nav class="hidden md:flex items-center gap-8 text-sm font-medium text-gray-400">
                <a href="#" class="text-white hover:text-indigo-400 transition-colors">Главная</a>
                <a href="#" class="hover:text-indigo-400 transition-colors">Топ-100</a>
                <a href="#" class="hover:text-indigo-400 transition-colors">Онгоинги</a>
                <a href="#" class="hover:text-indigo-400 transition-colors">Жанры</a>
            </nav>

            <!-- Поиск и Профиль -->
            <div class="flex items-center gap-4">
                <div class="relative hidden sm:block">
                    <input type="text" placeholder="Поиск аниме..." class="w-64 bg-gray-900/80 border border-gray-800 rounded-full py-1.5 pl-10 pr-4 text-sm text-gray-200 focus:outline-none focus:border-indigo-500 focus:ring-1 focus:ring-indigo-500 transition-all">
                    <i data-lucide="search" class="w-4 h-4 text-gray-500 absolute left-3.5 top-2.5"></i>
                </div>
                <button class="p-2 text-gray-400 hover:text-white sm:hidden">
                    <i data-lucide="search" class="w-5 h-5"></i>
                </button>
                <button class="flex items-center justify-center w-9 h-9 rounded-full bg-gray-800 hover:ring-2 hover:ring-indigo-500 transition-all overflow-hidden">
                    <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=100&q=80" alt="Аватар" class="w-full h-full object-cover">
                </button>
            </div>
        </div>
    </header>

    <!-- ГЛАВНЫЙ БАННЕР (HERO SECTION) -->
    <section class="relative pt-16 min-h-[75vh] flex items-center justify-center overflow-hidden">
        <!-- Задний фон с размытием -->
        <div class="absolute inset-0 z-0">
            <img src="https://images.unsplash.com/photo-1578632767115-351597cf2477?auto=format&fit=crop&w=1920&q=80" alt="Тренды" class="w-full h-full object-cover brightness-[0.25]">
            <div class="absolute inset-0 bg-gradient-to-t from-[#0b0c10] via-transparent to-[#0b0c10]/50"></div>
            <div class="absolute inset-0 bg-gradient-to-r from-[#0b0c10] via-transparent to-transparent"></div>
        </div>

        <!-- Контент баннера -->
        <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 w-full py-12">
            <div class="max-w-2xl">
                <div class="inline-flex items-center gap-2 bg-indigo-500/10 border border-indigo-500/30 text-indigo-400 px-3 py-1 rounded-full text-xs font-semibold uppercase tracking-wider mb-6 custom-blur">
                    <i data-lucide="trending-up" class="w-3.5 h-3.5"></i> Тренды сезона
                </div>
                <h1 class="text-4xl sm:text-6xl font-extrabold tracking-tight text-white mb-4 leading-tight">
                    Клинок рассекающий демонов
                </h1>
                <p class="text-base sm:text-lg text-gray-400 mb-8 line-clamp-3 leading-relaxed">
                    Тандзиро Камадо отправляется в опасное путешествие, чтобы найти способ вернуть человеческий облик своей сестре Нэдзуко, превращенной в демона, и отомстить за гибель своей семьи.
                </p>
                
                <div class="flex flex-wrap items-center gap-4">
                    <button class="flex items-center gap-2 bg-gradient-to-r from-indigo-600 to-purple-600 hover:from-indigo-500 hover:to-purple-500 text-white font-semibold px-6 py-3 rounded-xl shadow-lg shadow-indigo-600/30 active:scale-95 transition-all">
                        <i data-lucide="play" class="w-5 h-5 fill-white"></i> Смотреть 1 серию
                    </button>
                    <button class="flex items-center gap-2 bg-gray-800/80 hover:bg-gray-700/80 text-white font-medium px-5 py-3 rounded-xl border border-gray-700 custom-blur active:scale-95 transition-all">
                        <i data-lucide="bookmark" class="w-5 h-5"></i> В закладки
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- ОСНОВНОЙ КОНТЕНТ -->
    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 w-full py-12 flex-grow space-y-16">
        
        <!-- СЕКЦИЯ: ТРЕНДЫ (КАРТОЧКИ) -->
        <section>
            <div class="flex items-center justify-between mb-8">
                <div class="flex items-center gap-3">
                    <div class="w-1 h-6 bg-indigo-500 rounded-full"></div>
                    <h2 class="text-2xl font-bold tracking-tight text-white">Сейчас смотрят</h2>
                </div>
                <a href="#" class="text-sm font-semibold text-indigo-400 hover:text-indigo-300 flex items-center gap-1 group">
                    Все новинки <i data-lucide="chevron-right" class="w-4 h-4 group-hover:translate-x-0.5 transition-transform"></i>
                </a>
            </div>

            <!-- Сетка карточек -->
            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 gap-6">
                <!-- Карточка 1 -->
                <div class="group relative flex flex-col cursor-pointer">
                    <div class="relative aspect-[3/4] w-full rounded-2xl overflow-hidden bg-gray-900 shadow-md group-hover:shadow-indigo-500/10 transition-all">
                        <img src="https://images.unsplash.com/photo-1607604276583-eef5d076aa5f?auto=format&fit=crop&w=400&q=80" alt="Аниме" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
                            <div class="w-12 h-12 bg-white/10 custom-blur rounded-full flex items-center justify-center scale-75 group-hover:scale-100 transition-transform duration-300 border border-white/20">
                                <i data-lucide="play" class="w-5 h-5 text-white fill-white ml-0.5"></i>
                            </div>
                        </div>
                        <div class="absolute top-3 left-3 bg-indigo-600 text-[10px] font-bold px-2 py-0.5 rounded-md uppercase tracking-wider">HD</div>
                        <div class="absolute top-3 right-3 bg-black/60 custom-blur text-xs font-semibold px-2 py-0.5 rounded-md flex items-center gap-1 text-amber-400">
                            <i data-lucide="star" class="w-3 h-3 fill-amber-400"></i> 9.1
                        </div>
                    </div>
                    <h3 class="mt-3 font-semibold text-sm text-gray-200 group-hover:text-indigo-400 transition-colors line-clamp-1">Магическая битва</h3>
                    <p class="text-xs text-gray-500 mt-0.5">2 сезон • 23 серий</p>
                </div>

                <!-- Карточка 2 -->
                <div class="group relative flex flex-col cursor-pointer">
                    <div class="relative aspect-[3/4] w-full rounded-2xl overflow-hidden bg-gray-900 shadow-md group-hover:shadow-indigo-500/10 transition-all">
                        <img src="https://images.unsplash.com/photo-1560169897-fc0cdbdfa4d5?auto=format&fit=crop&w=400&q=80" alt="Аниме" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
                            <div class="w-12 h-12 bg-white/10 custom-blur rounded-full flex items-center justify-center scale-75 group-hover:scale-100 transition-transform duration-300 border border-white/20">
                                <i data-lucide="play" class="w-5 h-5 text-white fill-white ml-0.5"></i>
                            </div>
                        </div>
                        <div class="absolute top-3 left-3 bg-indigo-600 text-[10px] font-bold px-2 py-0.5 rounded-md uppercase tracking-wider">HD</div>
                        <div class="absolute top-3 right-3 bg-black/60 custom-blur text-xs font-semibold px-2 py-0.5 rounded-md flex items-center gap-1 text-amber-400">
                            <i data-lucide="star" class="w-3 h-3 fill-amber-400"></i> 8.8
                        </div>
                    </div>
                    <h3 class="mt-3 font-semibold text-sm text-gray-200 group-hover:text-indigo-400 transition-colors line-clamp-1">Атака титанов: Финал</h3>
                    <p class="text-xs text-gray-500 mt-0.5">4 сезон • 12 серий</p>
                </div>

                <!-- Карточка 3 -->
                <div class="group relative flex flex-col cursor-pointer">
                    <div class="relative aspect-[3/4] w-full rounded-2xl overflow-hidden bg-gray-900 shadow-md group-hover:shadow-indigo-500/10 transition-all">
                        <img src="https://images.unsplash.com/photo-1541562232579-512a21360020?auto=format&fit=crop&w=400&q=80" alt="Аниме" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
                            <div class="w-12 h-12 bg-white/10 custom-blur rounded-full flex items-center justify-center scale-75 group-hover:scale-100 transition-transform duration-300 border border-white/20">
                                <i data-lucide="play" class="w-5 h-5 text-white fill-white ml-0.5"></i>
                            </div>
                        </div>
                        <div class="absolute top-3 left-3 bg-indigo-600 text-[10px] font-bold px-2 py-0.5 rounded-md uppercase tracking-wider">HD</div>
                        <div class="absolute top-3 right-3 bg-black/60 custom-blur text-xs font-semibold px-2 py-0.5 rounded-md flex items-center gap-1 text-amber-400">
                            <i data-lucide="star" class="w-3 h-3 fill-amber-400"></i> 8.5
                        </div>
                    </div>
                    <h3 class="mt-3 font-semibold text-sm text-gray-200 group-hover:text-indigo-400 transition-colors line-clamp-1">Человек-бензопила</h3>
                    <p class="text-xs text-gray-500 mt-0.5">1 сезон • 12 серий</p>
                </div>

                <!-- Карточка 4 -->
                <div class="group relative flex flex-col cursor-pointer">
                    <div class="relative aspect-[3/4] w-full rounded-2xl overflow-hidden bg-gray-900 shadow-md group-hover:shadow-indigo-500/10 transition-all">
                        <img src="https://images.unsplash.com/photo-1528360983277-13d401cdc186?auto=format&fit=crop&w=400&q=80" alt="Аниме" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
                            <div class="w-12 h-12 bg-white/10 custom-blur rounded-full flex items-center justify-center scale-75 group-hover:scale-100 transition-transform duration-300 border border-white/20">
                                <i data-lucide="play" class="w-5 h-5 text-white fill-white ml-0.5"></i>
                            </div>
                        </div>
                        <div class="absolute top-3 left-3 bg-indigo-600 text-[10px] font-bold px-2 py-0.5 rounded-md uppercase tracking-wider">HD</div>
                        <div class="absolute top-3 right-3 bg-black/60 custom-blur text-xs font-semibold px-2 py-0.5 rounded-md flex items-center gap-1 text-amber-400">
                            <i data-lucide="star" class="w-3 h-3 fill-amber-400"></i> 9.4
                        </div>
                    </div>
                    <h3 class="mt-3 font-semibold text-sm text-gray-200 group-hover:text-indigo-400 transition-colors line-clamp-1">Провожающая в последний путь Фрирен</h3>
                    <p class="text-xs text-gray-500 mt-0.5">1 сезон • 28 серий</p>
                </div>

                <!-- Карточка 5 -->
                <div class="group relative flex flex-col cursor-pointer">
                    <div class="relative aspect-[3/4] w-full rounded-2xl overflow-hidden bg-gray-900 shadow-md group-hover:shadow-indigo-500/10 transition-all">
                        <img src="https://images.unsplash.com/photo-1534447677768-be436bb09401?auto=format&fit=crop&w=400&q=80" alt="Аниме" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
                            <div class="w-12 h-12 bg-white/10 custom-blur rounded-full flex items-center justify-center scale-75 group-hover:scale-100 transition-transform duration-300 border border-white/20">
                                <i data-lucide="play" class="w-5 h-5 text-white fill-white ml-0.5"></i>
                            </div>
                        </div>
                        <div class="absolute top-3 left-3 bg-indigo-600 text-[10px] font-bold px-2 py-0.5 rounded-md uppercase tracking-wider">HD</div>
                        <div class="absolute top-3 right-3 bg-black/60 custom-blur text-xs font-semibold px-2 py-0.5 rounded-md flex items-center gap-1 text-amber-400">
                            <i data-lucide="star" class="w-3 h-3 fill-amber-400"></i> 8.9
                        </div>
                    </div>
                    <h3 class="mt-3 font-semibold text-sm text-gray-200 group-hover:text-indigo-400 transition-colors line-clamp-1">Реинкарнация безработного</h3>
                    <p class="text-xs text-gray-500 mt-0.5">2 сезон • 24 серий</p>
                </div>
            </div>
        </section>

        <!-- СЕКЦИЯ: ПОСЛЕДНИЕ ОБНОВЛЕНИЯ СЕРИЙ -->
        <section>
            <div class="flex items-center gap-3 mb-8">
                <div class="w-1 h-6 bg-purple-500 rounded-full"></div>
                <h2 class="text-2xl font-bold tracking-tight text-white">Новые серии</h2>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
                <!-- Эпизод 1 -->
                <div class="bg-gray-900/40 border border-gray-800/60 rounded-xl p-3 flex items-center gap-4 hover:border-indigo-500/30 group cursor-pointer transition-colors">
                    <div class="relative w-28 aspect-video rounded-lg overflow-hidden flex-shrink-0 bg-gray-800">
                        <img src="https://images.unsplash.com/photo-1607604276583-eef5d076aa5f?auto=format&fit=crop&w=200&q=80" alt="Превью" class="w-full h-full object-cover">
                        <div class="absolute bottom-1 right-1 bg-black/70 text-[10px] px-1.5 py-0.5 rounded font-medium text-indigo-400">22 мин</div>
                    </div>
                    <div class="flex-grow min-w-0">
                        <h4 class="text-sm font-semibold text-gray-200 group-hover:text-indigo-400 transition-colors truncate">Магическая битва</h4>
                        <p class="text-xs text-gray-400 mt-1">Серия 18: «Шибуя»</p>
                        <span class="inline-block mt-2 text-[10px] bg-gray-800 text-gray-400 px-2 py-0.5 rounded">5 минут назад</span>
                    </div>
                </div>

                <!-- Эпизод 2 -->
                <div class="bg-gray-900/40 border border-gray-800/60 rounded-xl p-3 flex items-center gap-4 hover:border-indigo-500/30 group cursor-pointer transition-colors">
                    <div class="relative w-28 aspect-video rounded-lg overflow-hidden flex-shrink-0 bg-gray-800">
                        <img src="https://images.unsplash.com/photo-1541562232579-512a21360020?auto=format&fit=crop&w=200&q=80" alt="Превью" class="w-full h-full object-cover">
                        <div class="absolute bottom-1 right-1 bg-black/70 text-[10px] px-1.5 py-0.5 rounded font-medium text-indigo-400">24 мин</div>
                    </div>
                    <div class="flex-grow min-w-0">
                        <h4 class="text-sm font-semibold text-gray-200 group-hover:text-indigo-400 transition-colors truncate">Человек-бензопила</h4>
                        <p class="text-xs text-gray-400 mt-1">Серия 12: «Катана против Бензопилы»</p>
                        <span class="inline-block mt-2 text-[10px] bg-gray-800 text-gray-400 px-2 py-0.5 rounded">40 минут назад</span>
                    </div>
                </div>

                <!-- Эпизод 3 -->
                <div class="bg-gray-900/40 border border-gray-800/60 rounded-xl p-3 flex items-center gap-4 hover:border-indigo-500/30 group cursor-pointer transition-colors">
                    <div class="relative w-28 aspect-video rounded-lg overflow-hidden flex-shrink-0 bg-gray-800">
                        <img src="https://images.unsplash.com/photo-1534447677768-be436bb09401?auto=format&fit=crop&w=200&q=80" alt="Превью" class="w-full h-full object-cover">
                        <div class="absolute bottom-1 right-1 bg-black/70 text-[10px] px-1.5 py-0.5 rounded font-medium text-indigo-400">23 мин</div>
                    </div>
                    <div class="flex-grow min-w-0">
                        <h4 class="text-sm font-semibold text-gray-200 group-hover:text-indigo-400 transition-colors truncate">Реинкарнация безработного</h4>
                        <p class="text-xs text-gray-400 mt-1">Серия 3: «Отрезанный путь»</p>
                        <span class="inline-block mt-2 text-[10px] bg-gray-800 text-gray-400 px-2 py-0.5 rounded">1 час назад</span>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <!-- ПОДВАЛ (FOOTER) -->
    <footer class="bg-[#060709] border-t border-gray-900 py-8 mt-12 text-sm text-gray-500">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col sm:flex-row items-center justify-between gap-4">
            <div class="flex items-center gap-2">
                <span class="font-bold text-gray-400 tracking-wider">ANIMEDA</span>
                <span class="text-xs">&copy; 2026. Все права «защищены» стилем.</span>
            </div>
            <div class="flex gap-6">
                <a href="#" class="hover:text-gray-300 transition-colors">Правообладателям</a>
                <a href="#" class="hover:text-gray-300 transition-colors">Соглашение</a>
                <a href="#" class="hover:text-gray-300 transition-colors">Контакты</a>
            </div>
        </div>
    </footer>

    <!-- Скрипт инициализации иконок -->
    <script>
        lucide.createIcons();
    </script>
</body>
</html>
