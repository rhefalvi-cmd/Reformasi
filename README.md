
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MEI 1998: Ketika Indonesia Bergejolak</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts Inter & Merriweather -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=Merriweather:ital,wght@0,400;0,700;1,300&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brand: {
                            black: '#09090b',
                            dark: '#121215',
                            card: '#1a1a1e',
                            border: '#2e2e35',
                            red: '#dc2626',
                            brightred: '#ef4444',
                            darkred: '#991b1b',
                            gold: '#f59e0b'
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        serif: ['Merriweather', 'serif']
                    }
                }
            }
        }
    </script>
    <style>
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #09090b;
        }
        ::-webkit-scrollbar-thumb {
            background: #991b1b;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #dc2626;
        }
        
        .red-glow {
            text-shadow: 0 0 15px rgba(220, 38, 38, 0.6);
        }
        .box-glow {
            box-shadow: 0 0 25px rgba(220, 38, 38, 0.15);
        }
        .bg-grid-pattern {
            background-image: linear-gradient(to right, rgba(255,255,255,0.03) 1px, transparent 1px),
                              linear-gradient(to bottom, rgba(255,255,255,0.03) 1px, transparent 1px);
            background-size: 30px 30px;
        }
    </style>
</head>
<body class="bg-brand-black text-gray-200 font-sans antialiased selection:bg-brand-red selection:text-white min-h-screen flex flex-col justify-between">

    <!-- Navigation Bar -->
    <header class="sticky top-0 z-50 bg-brand-black/90 backdrop-blur-md border-b border-brand-border/60">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                <!-- Brand Logo -->
                <a href="#" class="flex items-center gap-3 group">
                    <div class="w-10 h-10 bg-gradient-to-br from-brand-red to-brand-darkred rounded-lg flex items-center justify-center text-white font-extrabold text-xl shadow-lg group-hover:scale-105 transition-transform">
                        98
                    </div>
                    <div class="flex flex-col">
                        <span class="font-black tracking-wider text-xl text-white group-hover:text-brand-red transition-colors uppercase">
                            REFORMASI <span class="text-brand-red">'98</span>
                        </span>
                        <span class="text-[10px] text-gray-400 font-mono tracking-widest uppercase">Tragedi & Fajar Baru</span>
                    </div>
                </a>

                <!-- Desktop Navigation Links -->
                <nav class="hidden md:flex items-center gap-6 text-sm font-medium">
                    <a href="#latar-belakang" class="hover:text-brand-red transition-colors py-1">Latar Belakang</a>
                    <a href="#kronologi" class="hover:text-brand-red transition-colors py-1">Kronologi</a>
                    <a href="#era-reformasi" class="hover:text-brand-red transition-colors py-1">Era Reformasi</a>
                    <a href="#dampak" class="hover:text-brand-red transition-colors py-1">Dampak</a>
                    <a href="#filsafat" class="hover:text-brand-red transition-colors py-1">Filsafat</a>
                    <a href="#galeri" class="hover:text-brand-red transition-colors py-1">Galeri Foto</a>
                </nav>

                <!-- Header Actions -->
                <div class="hidden sm:flex items-center gap-3">
                    <button onclick="toggleSearchModal()" class="p-2 text-gray-400 hover:text-white bg-brand-card hover:bg-brand-border rounded-lg border border-brand-border/80 transition-colors" title="Cari Topik">
                        <i class="fas fa-search"></i>
                    </button>
                </div>

                <!-- Mobile Menu Button -->
                <button id="mobile-menu-btn" onclick="toggleMobileMenu()" class="md:hidden p-2 text-gray-400 hover:text-white rounded-lg border border-brand-border bg-brand-card">
                    <i class="fas fa-bars text-xl" id="menu-icon"></i>
                </button>
            </div>
        </div>

        <!-- Mobile Menu Dropdown -->
        <div id="mobile-menu" class="hidden md:hidden bg-brand-dark border-b border-brand-border px-4 pt-2 pb-6 space-y-3 text-sm">
            <a href="#latar-belakang" onclick="toggleMobileMenu()" class="block py-2 text-gray-300 hover:text-brand-red border-b border-brand-border/40">Latar Belakang</a>
            <a href="#kronologi" onclick="toggleMobileMenu()" class="block py-2 text-gray-300 hover:text-brand-red border-b border-brand-border/40">Kronologi Peristiwa</a>
            <a href="#era-reformasi" onclick="toggleMobileMenu()" class="block py-2 text-gray-300 hover:text-brand-red border-b border-brand-border/40">Era Reformasi</a>
            <a href="#dampak" onclick="toggleMobileMenu()" class="block py-2 text-gray-300 hover:text-brand-red border-b border-brand-border/40">Dampak Peristiwa</a>
            <a href="#filsafat" onclick="toggleMobileMenu()" class="block py-2 text-gray-300 hover:text-brand-red border-b border-brand-border/40">Perspektif Filsafat</a>
            <a href="#galeri" onclick="toggleMobileMenu()" class="block py-2 text-gray-300 hover:text-brand-red">Galeri Dokumentasi</a>
        </div>
    </header>

    <!-- Hero Banner -->
    <section class="relative min-h-[85vh] flex items-center justify-center overflow-hidden bg-brand-black bg-grid-pattern py-16">
        <!-- Background Gradient Glows -->
        <div class="absolute top-1/4 left-1/2 -translate-x-1/2 w-96 h-96 bg-brand-red/20 rounded-full blur-[120px] pointer-events-none"></div>
        <div class="absolute bottom-0 left-0 w-full h-32 bg-gradient-to-t from-brand-black to-transparent pointer-events-none z-10"></div>

        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 relative z-20 text-center">
            <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-brand-red/10 border border-brand-red/30 text-brand-brightred text-xs font-semibold mb-6 tracking-wide">
                <span class="w-2 h-2 rounded-full bg-brand-brightred animate-ping"></span>
                DOKUMENTASI SEJARAH NASIONAL INDONESIA
            </div>

            <h1 class="text-4xl sm:text-6xl md:text-7xl font-black text-white tracking-tight uppercase leading-none mb-6">
                MEI 1998: KETIKA <br class="hidden sm:inline"/>
                <span class="text-transparent bg-clip-text bg-gradient-to-r from-brand-brightred via-red-500 to-red-800 red-glow">
                    INDONESIA BERGEJOLAK
                </span>
            </h1>

            <p class="max-w-3xl mx-auto text-base sm:text-xl text-gray-300 font-serif italic mb-10 leading-relaxed">
                "Dari Krisis dan Tragedi hingga Runtuhnya Orde Baru dan Lahirnya Era Reformasi"
            </p>

            <div class="flex flex-wrap items-center justify-center gap-4">
                <a href="#kronologi" class="bg-brand-red hover:bg-brand-darkred text-white font-bold text-sm px-8 py-4 rounded-xl shadow-lg shadow-red-900/40 hover:scale-105 transition-all flex items-center gap-3">
                    <i class="fas fa-hourglass-start"></i> Jelajahi Kronologi Mei '98
                </a>
                <a href="#filsafat" class="bg-brand-card hover:bg-brand-border text-gray-200 border border-brand-border font-semibold text-sm px-8 py-4 rounded-xl transition-all hover:text-white flex items-center gap-2">
                    <i class="fas fa-brain text-brand-brightred"></i> Analisis Filsafat
                </a>
            </div>

            <!-- Key Metric Cards -->
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mt-16 max-w-4xl mx-auto text-left">
                <div class="bg-brand-card/80 border border-brand-border p-4 rounded-xl backdrop-blur-sm">
                    <div class="text-3xl font-black text-brand-brightred">32 Tahun</div>
                    <div class="text-xs text-gray-400 mt-1 uppercase font-semibold">Masa Orde Baru Runtuh</div>
                </div>
                <div class="bg-brand-card/80 border border-brand-border p-4 rounded-xl backdrop-blur-sm">
                    <div class="text-3xl font-black text-brand-brightred">4 Martir</div>
                    <div class="text-xs text-gray-400 mt-1 uppercase font-semibold">Pahlawan Reformasi Trisakti</div>
                </div>
                <div class="bg-brand-card/80 border border-brand-border p-4 rounded-xl backdrop-blur-sm">
                    <div class="text-3xl font-black text-brand-brightred">12 - 21 Mei</div>
                    <div class="text-xs text-gray-400 mt-1 uppercase font-semibold">Puncak Puncak Peristiwa</div>
                </div>
                <div class="bg-brand-card/80 border border-brand-border p-4 rounded-xl backdrop-blur-sm">
                    <div class="text-3xl font-black text-brand-brightred">UU No. 9/98</div>
                    <div class="text-xs text-gray-400 mt-1 uppercase font-semibold">Tonggak Kebebasan Berekspresi</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Section A: Indonesia Menjelang Mei 1998 -->
    <section id="latar-belakang" class="py-20 bg-brand-dark border-t border-brand-border/60">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center gap-3 mb-4">
                <span class="w-10 h-1 bg-brand-red rounded-full"></span>
                <span class="text-brand-brightred font-mono text-sm tracking-widest font-bold uppercase">BAGIAN A</span>
            </div>
            <h2 class="text-3xl sm:text-4xl font-extrabold text-white mb-6">Indonesia Menjelang Mei 1998</h2>
            
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-10 items-center">
                <div class="lg:col-span-7 space-y-6 text-gray-300 leading-relaxed text-base sm:text-lg">
                    <p class="font-serif">
                        Memasuki tahun 1998, Indonesia berada dalam kondisi ekonomi dan politik yang sangat tidak stabil. Krisis finansial Asia yang bermula sejak pertengahan tahun 1997 menghantam sendi-sendi perekonomian nasional secara dahsyat.
                    </p>
                    
                    <div class="bg-brand-card border-l-4 border-brand-red p-5 rounded-r-xl my-4 space-y-3">
                        <h4 class="text-white font-bold text-lg flex items-center gap-2">
                            <i class="fas fa-chart-line-down text-brand-brightred"></i> Dampak Krisis Ekonomi:
                        </h4>
                        <ul class="space-y-2 text-sm text-gray-300">
                            <li class="flex items-start gap-2">
                                <i class="fas fa-caret-right text-brand-red mt-1"></i>
                                <span><strong>Pelemahan Rupiah:</strong> Nilai tukar rupiah terperosok tajam dari kisaran Rp2.500 menjadi belasan ribu per Dolar AS.</span>
                            </li>
                            <li class="flex items-start gap-2">
                                <i class="fas fa-caret-right text-brand-red mt-1"></i>
                                <span><strong>Lonjakan Sembako:</strong> Harga barang pokok melonjak drastis, menyebabkan kelangkaan dan kesulitan hidup rakyat.</span>
                            </li>
                            <li class="flex items-start gap-2">
                                <i class="fas fa-caret-right text-brand-red mt-1"></i>
                                <span><strong>Gelombang PHK:</strong> Penutupan industri dan bank memicu pengangguran massal secara cepat.</span>
                            </li>
                        </ul>
                    </div>

                    <p>
                        Krisis ekonomi tersebut kemudian berkembang pesat menjadi persoalan sosial dan politik yang masif. Ketidakpuasan masyarakat terhadap kepemimpinan Orde Baru yang telah berkuasa lebih dari 32 tahun kian memuncak. 
                    </p>
                    <p>
                        Mahasiswa dari berbagai perguruan tinggi di seluruh Indonesia mulai bergerak aktif di garda terdepan. Mereka menyuarakan gerakan Reformasi dengan tuntutan utama: <strong>perubahan politik nasional, penegakan hukum, serta pemberantasan Korupsi, Kolusi, dan Nepotisme (KKN).</strong> Demonstrasi yang awalnya terbatas di dalam kampus akhirnya meluap ke jalanan.
                    </p>
                </div>

                <!-- Visual Media Box -->
                <div class="lg:col-span-5">
                    <div class="relative group rounded-2xl overflow-hidden border border-brand-border bg-brand-card shadow-2xl">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSQsd-MJ3XoBNfQ8h0R8csLS7lpdEVgr0-d0VkfpsgrXA&s=10" 
                             alt="Aksi Unjuk Rasa Mahasiswa 1998" 
                             class="w-full h-80 sm:h-96 object-cover filter grayscale contrast-125 group-hover:grayscale-0 group-hover:scale-105 transition-all duration-500"
                             onerror="this.src='https://placehold.co/800x600/18181b/ffffff?text=Aksi+Demonstrasi+Mahasiswa+1998'">
                        <div class="absolute inset-0 bg-gradient-to-t from-brand-black via-brand-black/30 to-transparent"></div>
                        <div class="absolute bottom-0 left-0 right-0 p-6">
                            <span class="bg-brand-red text-white text-[10px] font-bold px-2.5 py-1 rounded tracking-wider uppercase mb-2 inline-block">Arsip Dokumentasi</span>
                            <p class="text-white font-semibold text-sm">Gelombang Aksi Demonstrasi Mahasiswa Menuntut Reformasi Total (1998)</p>
                            <p class="text-xs text-gray-400 mt-1">Suasana konsolidasi dan mobilisasi ribuan mahasiswa lintas perguruan tinggi.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Section B: Kronologi Tragedi Mei 1998 -->
    <section id="kronologi" class="py-20 bg-brand-black relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-brand-red/10 border border-brand-red/30 text-brand-brightred text-xs font-bold uppercase mb-3">
                    <i class="fas fa-calendar-alt"></i> BOLA SALJU PERISTIWA
                </div>
                <h2 class="text-3xl sm:text-5xl font-black text-white tracking-tight">Kronologi Tragedi Mei 1998</h2>
                <p class="text-gray-400 mt-3 text-base sm:text-lg">
                    Rangkaian peristiwa krusial selama 10 hari yang mengubah arah sejarah bangsa Indonesia selamanya.
                </p>
            </div>

            <!-- Timeline Filter Buttons -->
            <div class="flex flex-wrap justify-center gap-2 mb-12">
                <button onclick="filterTimeline('all')" class="tl-btn active bg-brand-red text-white text-xs sm:text-sm font-semibold px-4 py-2 rounded-lg border border-brand-red transition-all">Semua Peristiwa</button>
                <button onclick="filterTimeline('12may')" class="tl-btn bg-brand-card text-gray-300 hover:text-white text-xs sm:text-sm font-semibold px-4 py-2 rounded-lg border border-brand-border transition-all">12 Mei (Trisakti)</button>
                <button onclick="filterTimeline('13may')" class="tl-btn bg-brand-card text-gray-300 hover:text-white text-xs sm:text-sm font-semibold px-4 py-2 rounded-lg border border-brand-border transition-all">13-15 Mei (Kerusuhan)</button>
                <button onclick="filterTimeline('16may')" class="tl-btn bg-brand-card text-gray-300 hover:text-white text-xs sm:text-sm font-semibold px-4 py-2 rounded-lg border border-brand-border transition-all">16-19 Mei (Gedung DPR)</button>
                <button onclick="filterTimeline('20may')" class="tl-btn bg-brand-card text-gray-300 hover:text-white text-xs sm:text-sm font-semibold px-4 py-2 rounded-lg border border-brand-border transition-all">20 Mei (Ketegangan Monas)</button>
                <button onclick="filterTimeline('21may')" class="tl-btn bg-brand-card text-gray-300 hover:text-white text-xs sm:text-sm font-semibold px-4 py-2 rounded-lg border border-brand-border transition-all">21 Mei (Soeharto Mundur)</button>
            </div>

            <!-- Vertical Timeline Container -->
            <div class="relative border-l-2 border-brand-red/40 ml-4 sm:ml-32 md:ml-40 space-y-12">

                <!-- 1. Tragedi Trisakti (12 Mei) -->
                <div class="tl-item timeline-entry relative pl-8 sm:pl-10" data-category="12may">
                    <!-- Date Badge Desktop Floating -->
                    <div class="hidden sm:flex absolute -left-36 top-0 w-28 text-right flex-col">
                        <span class="text-xl font-black text-brand-brightred">12 MEI</span>
                        <span class="text-xs text-gray-400 font-mono">1998</span>
                    </div>

                    <!-- Node Icon -->
                    <div class="absolute -left-[17px] top-1 w-8 h-8 rounded-full bg-brand-red text-white flex items-center justify-center text-xs font-bold ring-4 ring-brand-black shadow-lg">
                        1
                    </div>

                    <div class="bg-brand-card border border-brand-border rounded-2xl p-6 sm:p-8 hover:border-brand-red/60 transition-all box-glow">
                        <div class="flex flex-wrap items-center justify-between gap-2 mb-3">
                            <span class="sm:hidden inline-block bg-brand-red/20 text-brand-brightred text-xs font-bold px-2.5 py-1 rounded font-mono">12 MEI 1998</span>
                            <h3 class="text-xl sm:text-2xl font-bold text-white">1. Tragedi Trisakti & Gugurnya Pahlawan Reformasi</h3>
                            <span class="text-xs bg-red-950 text-red-300 px-3 py-1 rounded-full border border-red-800/50">Titik Kritis</span>
                        </div>

                        <p class="text-gray-300 text-sm sm:text-base leading-relaxed mb-4">
                            Ribuan mahasiswa Universitas Trisakti menggelar aksi damai dari kampus menuju Gedung MPR/DPR. Aksi tertahan di luar area kampus akibat barikade aparat keamanan. Ketegangan bereskalasi saat petang hingga terdengar tembakan peluru tajam.
                        </p>

                        <!-- Martir Trisakti Callout Card -->
                        <div class="bg-brand-black/70 border border-brand-border p-4 rounded-xl my-4">
                            <h4 class="text-brand-brightred text-xs font-bold uppercase tracking-wider mb-3">Empat Mahasiswa Gugur (Pahlawan Reformasi):</h4>
                            <div class="grid grid-cols-2 sm:grid-cols-4 gap-3 text-center">
                                <div class="bg-brand-card p-2.5 rounded-lg border border-brand-border">
                                    <p class="text-white text-xs font-bold">Elang Mulia Lesmana</p>
                                    <p class="text-[10px] text-gray-400">Arsitektur '96</p>
                                </div>
                                <div class="bg-brand-card p-2.5 rounded-lg border border-brand-border">
                                    <p class="text-white text-xs font-bold">Heri Hertanto</p>
                                    <p class="text-[10px] text-gray-400">Teknik Mesin '95</p>
                                </div>
                                <div class="bg-brand-card p-2.5 rounded-lg border border-brand-border">
                                    <p class="text-white text-xs font-bold">Hafidin Royan</p>
                                    <p class="text-[10px] text-gray-400">Teknik Sipil '95</p>
                                </div>
                                <div class="bg-brand-card p-2.5 rounded-lg border border-brand-border">
                                    <p class="text-white text-xs font-bold">Hendriawan Sie</p>
                                    <p class="text-[10px] text-gray-400">Ekonomi '96</p>
                                </div>
                            </div>
                        </div>

                        <p class="text-xs text-gray-400 italic">
                            Kematian empat mahasiswa ini menjadi pemicu utama kemarahan publik berskala nasional yang memicu gelombang perlawanan tak tertahankan.
                        </p>
                    </div>
                </div>

                <!-- 2. Kerusuhan Meluas (13-15 Mei) -->
                <div class="tl-item timeline-entry relative pl-8 sm:pl-10" data-category="13may">
                    <div class="hidden sm:flex absolute -left-36 top-0 w-28 text-right flex-col">
                        <span class="text-xl font-black text-brand-brightred">13-15 MEI</span>
                        <span class="text-xs text-gray-400 font-mono">1998</span>
                    </div>

                    <div class="absolute -left-[17px] top-1 w-8 h-8 rounded-full bg-brand-red text-white flex items-center justify-center text-xs font-bold ring-4 ring-brand-black shadow-lg">
                        2
                    </div>

                    <div class="bg-brand-card border border-brand-border rounded-2xl p-6 sm:p-8 hover:border-brand-red/60 transition-all">
                        <div class="flex flex-wrap items-center justify-between gap-2 mb-3">
                            <span class="sm:hidden inline-block bg-brand-red/20 text-brand-brightred text-xs font-bold px-2.5 py-1 rounded font-mono">13-15 MEI 1998</span>
                            <h3 class="text-xl sm:text-2xl font-bold text-white">2. Kerusuhan Meluas & Tragedi Kemanusiaan</h3>
                            <span class="text-xs bg-gray-800 text-gray-300 px-3 py-1 rounded-full border border-gray-700">Tragedi Sosial</span>
                        </div>

                        <p class="text-gray-300 text-sm sm:text-base leading-relaxed mb-4">
                            Pasca peristiwa Trisakti, situasi di Jakarta dan kota-kota besar lainnya (seperti Surakarta, Medan, Surabaya) lepas kendali. Terjadi penjarahan, pembakaran pusat perbelanjaan, perusakan fasos-fasum, serta tindak kekerasan rasial.
                        </p>

                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 my-4">
                            <div class="bg-brand-black/60 p-4 rounded-xl border border-brand-border">
                                <h5 class="text-white font-bold text-xs uppercase text-brand-brightred mb-1">Kekerasan Rasial & Penjarahan</h5>
                                <p class="text-xs text-gray-300">Target penjarahan dan perusakan merembet pada toko dan aset warga keturunan Tionghoa, menimbulkan luka trauma sosial mendalam dan dampak kemanusiaan luar biasa.</p>
                            </div>
                            <div class="bg-brand-black/60 p-4 rounded-xl border border-brand-border">
                                <h5 class="text-white font-bold text-xs uppercase text-brand-brightred mb-1">Pembentukan TGPF</h5>
                                <p class="text-xs text-gray-300">Pemerintah kemudian membentuk <em>Tim Gabungan Pencari Fakta (TGPF)</em> untuk menyelidiki fakta lapangan, korban jiwa, serta motif kerusuhan sistematis tersebut.</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 3. Tuntutan Reformasi Semakin Kuat (16-19 Mei) -->
                <div class="tl-item timeline-entry relative pl-8 sm:pl-10" data-category="16may">
                    <div class="hidden sm:flex absolute -left-36 top-0 w-28 text-right flex-col">
                        <span class="text-xl font-black text-brand-brightred">16-19 MEI</span>
                        <span class="text-xs text-gray-400 font-mono">1998</span>
                    </div>

                    <div class="absolute -left-[17px] top-1 w-8 h-8 rounded-full bg-brand-red text-white flex items-center justify-center text-xs font-bold ring-4 ring-brand-black shadow-lg">
                        3
                    </div>

                    <div class="bg-brand-card border border-brand-border rounded-2xl p-6 sm:p-8 hover:border-brand-red/60 transition-all">
                        <div class="flex flex-wrap items-center justify-between gap-2 mb-3">
                            <span class="sm:hidden inline-block bg-brand-red/20 text-brand-brightred text-xs font-bold px-2.5 py-1 rounded font-mono">16-19 MEI 1998</span>
                            <h3 class="text-xl sm:text-2xl font-bold text-white">3. Pengudayaan Gedung MPR/DPR oleh Mahasiswa</h3>
                        </div>

                        <p class="text-gray-300 text-sm sm:text-base leading-relaxed mb-4">
                            Redanya kerusuhan tidak menyurutkan perlawanan. Puluhan ribu mahasiswa dengan jaket almamater berwarna-warni dari berbagai penjuru Tanah Air mendatangi dan menduduki Kompleks Gedung MPR/DPR di Senayan, Jakarta.
                        </p>

                        <div class="bg-brand-black/80 border border-brand-border p-4 rounded-xl flex items-center gap-4">
                            <div class="p-3 bg-brand-red/20 rounded-lg text-brand-brightred text-2xl">
                                <i class="fas fa-landmark"></i>
                            </div>
                            <div class="text-xs text-gray-300">
                                Mahasiswa berkemah, menginap, dan memanjat kubah hijau ikonik DPR RI. Tuntutan tunggal menggaung keras: <strong>Soeharto Harus Mundur dari Jabatan Presiden RI!</strong>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 4. Jakarta Dalam Ketegangan (20 Mei) -->
                <div class="tl-item timeline-entry relative pl-8 sm:pl-10" data-category="20may">
                    <div class="hidden sm:flex absolute -left-36 top-0 w-28 text-right flex-col">
                        <span class="text-xl font-black text-brand-brightred">20 MEI</span>
                        <span class="text-xs text-gray-400 font-mono">1998</span>
                    </div>

                    <div class="absolute -left-[17px] top-1 w-8 h-8 rounded-full bg-brand-red text-white flex items-center justify-center text-xs font-bold ring-4 ring-brand-black shadow-lg">
                        4
                    </div>

                    <div class="bg-brand-card border border-brand-border rounded-2xl p-6 sm:p-8 hover:border-brand-red/60 transition-all">
                        <div class="flex flex-wrap items-center justify-between gap-2 mb-3">
                            <span class="sm:hidden inline-block bg-brand-red/20 text-brand-brightred text-xs font-bold px-2.5 py-1 rounded font-mono">20 MEI 1998</span>
                            <h3 class="text-xl sm:text-2xl font-bold text-white">4. Peringatan Harkitnas & Barikade Militer Jakarta</h3>
                        </div>

                        <p class="text-gray-300 text-sm sm:text-base leading-relaxed mb-4">
                            Direncanakan aksi akselerasi massa besar-besaran memperingati Hari Kebangkitan Nasional di kawasan Monas. Namun, aparat keamanan mengisolasi Monas dengan kawat berduri, tank, dan kendaraan lapis baja.
                        </p>

                        <p class="text-xs text-gray-300 bg-brand-black/60 p-3 rounded-lg border border-brand-border">
                            Tokoh reformasi Amien Rais membatalkan rencana rapat akbar di Monas guna menghindari pertumpahan darah. Konsentrasi massa sepenuhnya beralih mengepung Kompleks Senayan.
                        </p>
                    </div>
                </div>

                <!-- 5. Soeharto Mengundurkan Diri (21 Mei) -->
                <div class="tl-item timeline-entry relative pl-8 sm:pl-10" data-category="21may">
                    <div class="hidden sm:flex absolute -left-36 top-0 w-28 text-right flex-col">
                        <span class="text-xl font-black text-brand-brightred">21 MEI</span>
                        <span class="text-xs text-gray-400 font-mono">1998</span>
                    </div>

                    <div class="absolute -left-[17px] top-1 w-8 h-8 rounded-full bg-brand-brightred text-white flex items-center justify-center text-xs font-bold ring-4 ring-brand-black shadow-lg animate-bounce">
                        <i class="fas fa-flag"></i>
                    </div>

                    <div class="bg-gradient-to-br from-brand-card to-brand-darkred/20 border-2 border-brand-red rounded-2xl p-6 sm:p-8 box-glow">
                        <div class="flex flex-wrap items-center justify-between gap-2 mb-3">
                            <span class="sm:hidden inline-block bg-brand-red text-white text-xs font-bold px-2.5 py-1 rounded font-mono">21 MEI 1998</span>
                            <h3 class="text-2xl sm:text-3xl font-black text-white">5. Soeharto Mundur & Fajar Era Reformasi</h3>
                            <span class="text-xs bg-brand-red text-white font-bold px-3 py-1 rounded-full uppercase">Puncak Sejarah</span>
                        </div>

                        <p class="text-gray-200 text-sm sm:text-base leading-relaxed mb-4 font-serif">
                            Pukul 09.00 WIB di Istana Merdeka, Presiden Soeharto membacakan pernyataan mengundurkan diri dari jabatannya setelah 32 tahun memimpin Indonesia.
                        </p>

                        <div class="bg-brand-black/90 p-4 rounded-xl border border-brand-border text-xs sm:text-sm text-gray-300 space-y-2">
                            <p>
                                <i class="fas fa-quote-left text-brand-brightred mr-2"></i>
                                <em>"Saya memutuskan untuk menyatakan berhenti dari jabatan saya sebagai Presiden Republik Indonesia..."</em>
                            </p>
                            <p class="pt-2 border-t border-brand-border/60 text-gray-400">
                                Sesuai Pasal 8 UUD 1945, Wakil Presiden <strong>B.J. Habibie</strong> langsung dilantik menjadi Presiden ke-3 Republik Indonesia. Pengunduran diri ini secara resmi mengakhiri Era Orde Baru.
                            </p>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Section C & D: Era Reformasi & Dampak Tragedi -->
    <section id="era-reformasi" class="py-20 bg-brand-dark border-t border-brand-border/60">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            
            <!-- Section C Header -->
            <div class="mb-16">
                <div class="flex items-center gap-3 mb-2">
                    <span class="w-10 h-1 bg-brand-red rounded-full"></span>
                    <span class="text-brand-brightred font-mono text-sm tracking-widest font-bold uppercase">BAGIAN C</span>
                </div>
                <h2 class="text-3xl sm:text-4xl font-black text-white mb-4">Awal Era Reformasi</h2>
                <p class="text-gray-300 max-w-3xl text-base leading-relaxed">
                    Pengunduran diri Soeharto tidak otomatis menyelesaikan seluruh permasalahan bangsa. Pemerintahan baru B.J. Habibie harus meletakkan fondasi transisi demokrasi di tengah krisis multidimensional.
                </p>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-8">
                    <div class="bg-brand-card p-6 rounded-2xl border border-brand-border hover:border-brand-red transition-all">
                        <div class="w-12 h-12 bg-brand-red/20 text-brand-brightred rounded-xl flex items-center justify-center text-xl font-bold mb-4">
                            <i class="fas fa-bullhorn"></i>
                        </div>
                        <h3 class="text-white font-bold text-lg mb-2">UU No. 9 Tahun 1998</h3>
                        <p class="text-gray-400 text-sm">Lahirnya regulasi jaminan kebebasan menyampaikan pendapat di muka umum secara legal dan terbuka.</p>
                    </div>

                    <div class="bg-brand-card p-6 rounded-2xl border border-brand-border hover:border-brand-red transition-all">
                        <div class="w-12 h-12 bg-brand-red/20 text-brand-brightred rounded-xl flex items-center justify-center text-xl font-bold mb-4">
                            <i class="fas fa-box-archive"></i>
                        </div>
                        <h3 class="text-white font-bold text-lg mb-2">Kebebasan Pers & Partai</h3>
                        <p class="text-gray-400 text-sm">Penghapusan SIUPP (Bredel pers) serta pembukaan keran sistem multipartai untuk pemilu demokratis 1999.</p>
                    </div>

                    <div class="bg-brand-card p-6 rounded-2xl border border-brand-border hover:border-brand-red transition-all">
                        <div class="w-12 h-12 bg-brand-red/20 text-brand-brightred rounded-xl flex items-center justify-center text-xl font-bold mb-4">
                            <i class="fas fa-scale-balanced"></i>
                        </div>
                        <h3 class="text-white font-bold text-lg mb-2">Reformasi Hukum & Kebijakan</h3>
                        <p class="text-gray-400 text-sm">Restrukturisasi perbankan, otonomi daerah, serta pelepasan tahanan politik Orde Baru.</p>
                    </div>
                </div>
            </div>

            <!-- Section D: Dampak Tragedi Mei 1998 -->
            <div id="dampak" class="pt-10 border-t border-brand-border/40">
                <div class="flex items-center gap-3 mb-2">
                    <span class="w-10 h-1 bg-brand-red rounded-full"></span>
                    <span class="text-brand-brightred font-mono text-sm tracking-widest font-bold uppercase">BAGIAN D</span>
                </div>
                <h2 class="text-3xl sm:text-4xl font-black text-white mb-8">Dampak Tragedi Mei 1998</h2>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <!-- 1. Dampak Sosial -->
                    <div class="bg-brand-card p-6 rounded-2xl border border-brand-border">
                        <div class="text-brand-brightred text-2xl font-black mb-3 flex items-center justify-between">
                            <span>01. Sosial</span>
                            <i class="fas fa-users text-gray-600"></i>
                        </div>
                        <p class="text-gray-300 text-sm leading-relaxed">
                            Meninggalkan trauma psikologis mendalam, rasa tidak aman, serta duka cita akibat tindak kekerasan rasial. Peristiwa ini membuka mata publik pentingnya perlindungan hak asasi manusia dan kebhinekaan.
                        </p>
                    </div>

                    <!-- 2. Dampak Ekonomi -->
                    <div class="bg-brand-card p-6 rounded-2xl border border-brand-border">
                        <div class="text-brand-brightred text-2xl font-black mb-3 flex items-center justify-between">
                            <span>02. Ekonomi</span>
                            <i class="fas fa-store-slash text-gray-600"></i>
                        </div>
                        <p class="text-gray-300 text-sm leading-relaxed">
                            Kerusakan sarana usaha, pembakaran pusat pertokoan, dan kerugian riil triliunan rupiah. Dibutuhkan waktu bertahun-tahun untuk mengembalikan kepercayaan investor asing dan memulihkan kegiatan ekonomi.
                        </p>
                    </div>

                    <!-- 3. Dampak Politik -->
                    <div class="bg-brand-card p-6 rounded-2xl border border-brand-border">
                        <div class="text-brand-brightred text-2xl font-black mb-3 flex items-center justify-between">
                            <span>03. Politik</span>
                            <i class="fas fa-monument text-gray-600"></i>
                        </div>
                        <p class="text-gray-300 text-sm leading-relaxed">
                            Runtuhnya rezim otoriter Orde Baru 32 tahun, pergeseran dari sistem sentralistik menuju desentralisasi otonomi daerah, serta dimulainya iklim tata kelola negara yang lebih terbuka dan transparan.
                        </p>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <!-- Section E: Mei 1998 Dalam Perspektif Filsafat -->
    <section id="filsafat" class="py-20 bg-brand-black border-t border-brand-border">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-12">
                <span class="text-brand-brightred font-mono text-sm tracking-widest font-bold uppercase">BAGIAN E</span>
                <h2 class="text-3xl sm:text-5xl font-black text-white mt-2">Tinjauan Perspektif Filsafat</h2>
                <p class="text-gray-400 mt-3 text-sm sm:text-base">
                    Memahami peristiwa Mei 1998 tidak sekadar mencatat tanggal, melainkan menelaah hakikat (Ontologi), sumber pengetahuan (Epistemologi), dan nilai-nilai kemanusiaan (Aksiologi).
                </p>
            </div>

            <!-- Tab Buttons -->
            <div class="flex justify-center border-b border-brand-border mb-8">
                <button onclick="switchTab('ontologi')" id="tab-ontologi" class="tab-btn active px-6 py-3 font-bold text-sm sm:text-base border-b-2 border-brand-red text-white transition-all">
                    1. Ontologi
                </button>
                <button onclick="switchTab('epistemologi')" id="tab-epistemologi" class="tab-btn px-6 py-3 font-bold text-sm sm:text-base border-b-2 border-transparent text-gray-400 hover:text-white transition-all">
                    2. Epistemologi
                </button>
                <button onclick="switchTab('aksiologi')" id="tab-aksiologi" class="tab-btn px-6 py-3 font-bold text-sm sm:text-base border-b-2 border-transparent text-gray-400 hover:text-white transition-all">
                    3. Aksiologi
                </button>
            </div>

            <!-- Tab Content Cards -->
            <div class="max-w-4xl mx-auto">
                <!-- Tab 1: Ontologi -->
                <div id="content-ontologi" class="tab-content block bg-brand-card border border-brand-border p-8 rounded-2xl">
                    <div class="flex items-center gap-3 mb-4">
                        <i class="fas fa-cubes text-brand-brightred text-2xl"></i>
                        <h3 class="text-2xl font-bold text-white">Ontologi: Apa Hakikat Peristiwa Mei 1998?</h3>
                    </div>
                    <p class="text-gray-300 leading-relaxed font-serif text-base mb-4">
                        Secara ontologis, Mei 1998 tidak dapat disempitkan hanya sebagai sebuah kerusuhan biasa. Peristiwa ini merupakan suatu <strong>fenomena sejarah kompleks</strong> yang saling berkelindan antara krisis ekonomi global, gerakan perlawanan mahasiswa, ketegangan elite politik, kekerasan sosial, hingga pergeseran struktur kekuasaan nasional.
                    </p>
                    <p class="text-gray-400 text-sm">
                        Hakikat Mei 1998 adalah cermin dialektika hubungan antara ketidakadilan sosial-ekonomi, akumulasi kekuasaan yang tak terkontrol, serta daya dorong perubahan dalam masyarakat.
                    </p>
                </div>

                <!-- Tab 2: Epistemologi -->
                <div id="content-epistemologi" class="tab-content hidden bg-brand-card border border-brand-border p-8 rounded-2xl">
                    <div class="flex items-center gap-3 mb-4">
                        <i class="fas fa-book-open-reader text-brand-brightred text-2xl"></i>
                        <h3 class="text-2xl font-bold text-white">Epistemologi: Bagaimana Kita Mengetahui Peristiwa Ini?</h3>
                    </div>
                    <p class="text-gray-300 leading-relaxed font-serif text-base mb-4">
                        Pengetahuan historis mengenai Mei 1998 diverifikasi dan dikonstruksi melalui berbagai instrumen sumber bukti sejarah: <strong>arsip koran, rekaman audiovisual, laporan investigasi resmi (TGPF), kesaksian penyintas, serta studi akademik.</strong>
                    </p>
                    <p class="text-gray-400 text-sm">
                        Epistemologi mengarahkan kita untuk kritis membandingkan pelbagai sumber informasi, menghindari sudut pandang tunggal, serta melakukan analisis hermeneutika terhadap jejak fakta sejarah secara obyektif.
                    </p>
                </div>

                <!-- Tab 3: Aksiologi -->
                <div id="content-aksiologi" class="tab-content hidden bg-brand-card border border-brand-border p-8 rounded-2xl">
                    <div class="flex items-center gap-3 mb-4">
                        <i class="fas fa-heart-pulse text-brand-brightred text-2xl"></i>
                        <h3 class="text-2xl font-bold text-white">Aksiologi: Apa Nilai & Kegunaan Bagi Masa Kini?</h3>
                    </div>
                    <p class="text-gray-300 leading-relaxed font-serif text-base mb-4">
                        Aspek aksiologis memberikan fondasi etis. Mempelajari Mei 1998 bernilai tinggi untuk memupuk keinsafan akan <strong>pentingnya demokrasi, perlindungan HAM, penghormatan atas keberagaman ras/etnis, serta penyelesaian konflik tanpa kekerasan.</strong>
                    </p>
                    <p class="text-gray-400 text-sm">
                        Nilai pragmatisnya mengingatkan generasi penerus bahwa kebebasan politik yang dinikmati hari ini dibayar mahal oleh pengorbanan jiwa dan raga para pahlawan reformasi.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Section: Galeri Dokumentasi Foto -->
    <section id="galeri" class="py-20 bg-brand-dark border-t border-brand-border/60">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-12">
                <div>
                    <span class="text-brand-brightred font-mono text-sm tracking-widest font-bold uppercase">DOKUMENTASI HISTORIS</span>
                    <h2 class="text-3xl sm:text-4xl font-black text-white mt-1">Galeri Foto Reformasi 1998</h2>
                </div>
                <p class="text-gray-400 text-sm max-w-md mt-2 md:mt-0">
                    Klik pada gambar untuk memperbesar dokumentasi foto arsip seputar peristiwa Mei 1998.
                </p>
            </div>

            <!-- Gallery Grid -->
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
                <!-- Image 1 -->
                <div onclick="openLightbox('https://upload.wikimedia.org/wikipedia/commons/thumb/d/d4/Indonesian_student_demonstrators_occupy_the_Parliament_building.jpg/800px-Indonesian_student_demonstrators_occupy_the_Parliament_building.jpg', 'Pendudukan Gedung MPR/DPR oleh Puluhan Ribu Mahasiswa (Mei 1998)')" 
                     class="group relative rounded-xl overflow-hidden bg-brand-card border border-brand-border cursor-pointer aspect-video shadow-lg">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTMdR3rTmCitQfXAxSAA5fnKaAO8-HZGjiOcx68ImD_5VBEvXwJvZ428N0&s=10" 
                         alt="Mahasiswa di DPR" 
                         class="w-full h-full object-cover filter grayscale group-hover:grayscale-0 group-hover:scale-110 transition-all duration-500"
                         onerror="this.src='https://placehold.co/800x600/18181b/ffffff?text=Pendudukan+Gedung+DPR+1998'">
                    <div class="absolute inset-0 bg-gradient-to-t from-brand-black via-transparent to-transparent opacity-80"></div>
                    <div class="absolute bottom-0 p-4">
                        <p class="text-white text-xs font-bold">Pendudukan Gedung MPR/DPR Senayan</p>
                        <p class="text-[10px] text-gray-400">Ribuan mahasiswa menguasai kubah DPR/MPR</p>
                    </div>
                </div>

                <!-- Image 2 -->
                <div onclick="openLightbox('https://upload.wikimedia.org/wikipedia/commons/thumb/2/22/Suharto_resignation.jpg/800px-Suharto_resignation.jpg', 'Presiden Soeharto Membacakan Teks Pengunduran Diri di Istana Merdeka (21 Mei 1998)')" 
                     class="group relative rounded-xl overflow-hidden bg-brand-card border border-brand-border cursor-pointer aspect-video shadow-lg">
                    <img src="https://asset.kompas.com/crops/x611YVCVgwO1G-BI3DmnrXEU5sY=/20x0:743x482/1200x800/data/photo/2018/05/20/554933080.jpg" 
                         alt="Pidato Mundur Soeharto" 
                         class="w-full h-full object-cover filter grayscale group-hover:grayscale-0 group-hover:scale-110 transition-all duration-500"
                         onerror="this.src='https://placehold.co/800x600/18181b/ffffff?text=Pidato+Mundur+Soeharto+21+Mei'">
                    <div class="absolute inset-0 bg-gradient-to-t from-brand-black via-transparent to-transparent opacity-80"></div>
                    <div class="absolute bottom-0 p-4">
                        <p class="text-white text-xs font-bold">Pengunduran Diri Soeharto</p>
                        <p class="text-[10px] text-gray-400">Pernyataan resmi di Istana Merdeka, 21 Mei 1998</p>
                    </div>
                </div>

                <!-- Image 3 -->
                <div onclick="openLightbox('https://images.unsplash.com/photo-1578898835028-267b093f0a4f?auto=format&fit=crop&w=1000&q=80', 'Suasana Ketegangan Kota Jakarta dan Penjagaan Keamanan (1998)')" 
                     class="group relative rounded-xl overflow-hidden bg-brand-card border border-brand-border cursor-pointer aspect-video shadow-lg">
                    <img src="https://static.dw.com/image/69041980_902.jpg" 
                         alt="Ketegangan Kota Jakarta" 
                         class="w-full h-full object-cover filter grayscale group-hover:grayscale-0 group-hover:scale-110 transition-all duration-500"
                         onerror="this.src='https://placehold.co/800x600/18181b/ffffff?text=Situasi+Jakarta+1998'">
                    <div class="absolute inset-0 bg-gradient-to-t from-brand-black via-transparent to-transparent opacity-80"></div>
                    <div class="absolute bottom-0 p-4">
                        <p class="text-white text-xs font-bold">Barikade & Pengamanan</p>
                        <p class="text-[10px] text-gray-400">Penjagaan ketat di sudut-sudut strategis Jakarta</p>
                    </div>
                </div>

                <!-- Image 4 -->
                <div onclick="openLightbox('https://upload.wikimedia.org/wikipedia/commons/thumb/e/e4/DPR_RI_Building_Complex.jpg/800px-DPR_RI_Building_Complex.jpg', 'Kompleks Gedung DPR RI Senayan Tempat Berkumpulnya Mahasiswa')" 
                     class="group relative rounded-xl overflow-hidden bg-brand-card border border-brand-border cursor-pointer aspect-video shadow-lg">
                    <img src="https://manunggal.undip.ac.id/wp-content/uploads/2026/05/WhatsApp-Image-2026-05-21-at-06.58.08.jpeg" 
                         alt="Gedung DPR RI" 
                         class="w-full h-full object-cover filter grayscale group-hover:grayscale-0 group-hover:scale-110 transition-all duration-500"
                         onerror="this.src='https://placehold.co/800x600/18181b/ffffff?text=Gedung+DPR+RI'">
                    <div class="absolute inset-0 bg-gradient-to-t from-brand-black via-transparent to-transparent opacity-80"></div>
                    <div class="absolute bottom-0 p-4">
                        <p class="text-white text-xs font-bold">Gedung DPR/MPR RI</p>
                        <p class="text-[10px] text-gray-400">Pusat simbol pengerahan gerakan mahasiswa 1998</p>
                    </div>
                </div>

                <!-- Image 5 -->
                <div onclick="openLightbox('https://images.unsplash.com/photo-1541872703-74c5e44368f9?auto=format&fit=crop&w=1000&q=80', 'Aksi Unjuk Rasa Menuntut Pemberantasan KKN & Reformasi Total')" 
                     class="group relative rounded-xl overflow-hidden bg-brand-card border border-brand-border cursor-pointer aspect-video shadow-lg">
                    <img src="https://c.files.bbci.co.uk/BC7F/production/_101655284_003dc7c0-8620-4e08-92ab-8d3f7c7f5571.jpg" 
                         alt="Demonstrasi Mahasiswa" 
                         class="w-full h-full object-cover filter grayscale group-hover:grayscale-0 group-hover:scale-110 transition-all duration-500"
                         onerror="this.src='https://placehold.co/800x600/18181b/ffffff?text=Orasi+Reformasi'">
                    <div class="absolute inset-0 bg-gradient-to-t from-brand-black via-transparent to-transparent opacity-80"></div>
                    <div class="absolute bottom-0 p-4">
                        <p class="text-white text-xs font-bold">Orasi & Tuntutan Reformasi</p>
                        <p class="text-[10px] text-gray-400">Seruan penghapusan KKN dan kebebasan demokrasi</p>
                    </div>
                </div>

                <!-- Image 6 -->
                <div onclick="openLightbox('https://images.unsplash.com/photo-1589829545856-d10d557cf95f?auto=format&fit=crop&w=1000&q=80', 'Simbolisasi Keadilan dan Supremasi Hukum Pasca Mei 1998')" 
                     class="group relative rounded-xl overflow-hidden bg-brand-card border border-brand-border cursor-pointer aspect-video shadow-lg">
                    <img src="https://asset.kompas.com/crops/LWPELc7ovEKXoaT7T1oVGxrEDtY=/217x0:915x465/750x500/data/photo/2020/02/10/5e416ce1b16a5.png" 
                         alt="Supremasi Hukum Reformasi" 
                         class="w-full h-full object-cover filter grayscale group-hover:grayscale-0 group-hover:scale-110 transition-all duration-500"
                         onerror="this.src='https://placehold.co/800x600/18181b/ffffff?text=Penegakan+Hukum'">
                    <div class="absolute inset-0 bg-gradient-to-t from-brand-black via-transparent to-transparent opacity-80"></div>
                    <div class="absolute bottom-0 p-4">
                        <p class="text-white text-xs font-bold">Penegakan Supremasi Hukum</p>
                        <p class="text-[10px] text-gray-400">Fondasi baru sistem perundang-undangan nasional</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-brand-dark border-t border-brand-border py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row items-center justify-between gap-6">
                
                <div class="flex items-center gap-3">
                    <div class="w-8 h-8 bg-brand-red rounded flex items-center justify-center font-bold text-white text-sm">
                        98
                    </div>
                    <div>
                        <p class="text-white font-bold text-sm">Portal Sejarah Reformasi 1998</p>
                        <p class="text-xs text-gray-400">Materi Edukasi Gerakan Kebangsaan & Nilai Pancasila</p>
                    </div>
                </div>

                <p class="text-xs text-gray-400 text-center">
                    &copy; 1998 - 2026 Edukasi Sejarah Indonesia. Disusun berdasarkan Dokumen GKN "Mei 1998: Ketika Indonesia Bergejolak".
                </p>

                <div class="flex items-center gap-4">
                    <button onclick="window.scrollTo({top:0, behavior:'smooth'})" class="p-2.5 bg-brand-card hover:bg-brand-border rounded-lg text-gray-400 hover:text-white border border-brand-border transition-colors text-xs flex items-center gap-2">
                        <i class="fas fa-arrow-up"></i> Ke Atas
                    </button>
                </div>

            </div>
        </div>
    </footer>

    <!-- Lightbox Modal for Photo Preview -->
    <div id="lightbox-modal" class="fixed inset-0 z-50 bg-black/90 backdrop-blur-md hidden flex items-center justify-center p-4">
        <div class="relative max-w-4xl w-full bg-brand-card rounded-2xl border border-brand-border overflow-hidden">
            <button onclick="closeLightbox()" class="absolute top-4 right-4 z-10 w-10 h-10 bg-black/60 text-white rounded-full flex items-center justify-center hover:bg-brand-red transition-colors">
                <i class="fas fa-xmark text-lg"></i>
            </button>
            <div class="p-2 bg-black flex items-center justify-center max-h-[70vh]">
                <img id="lightbox-img" src="" alt="Enlarged view" class="max-h-[65vh] object-contain rounded">
            </div>
            <div class="p-4 bg-brand-card">
                <p id="lightbox-caption" class="text-white text-sm font-semibold"></p>
            </div>
        </div>
    </div>

    <!-- Search Modal -->
    <div id="search-modal" class="fixed inset-0 z-50 bg-black/80 backdrop-blur-sm hidden items-center justify-center p-4">
        <div class="bg-brand-card border border-brand-border w-full max-w-lg rounded-2xl p-6 shadow-2xl">
            <div class="flex items-center justify-between mb-4">
                <h3 class="text-white font-bold text-lg"><i class="fas fa-search text-brand-brightred mr-2"></i> Cari Materi Sejarah</h3>
                <button onclick="toggleSearchModal()" class="text-gray-400 hover:text-white"><i class="fas fa-times"></i></button>
            </div>
            <input type="text" id="search-input" onkeyup="performSearch()" placeholder="Ketik kata kunci (misal: Trisakti, Soeharto, Habibie, Monas)..." 
                   class="w-full bg-brand-black border border-brand-border rounded-xl px-4 py-3 text-white text-sm focus:outline-none focus:border-brand-red mb-4">
            <div id="search-results" class="max-h-60 overflow-y-auto space-y-2 text-xs text-gray-300">
                <!-- Search results injected dynamically -->
            </div>
        </div>
    </div>

    <!-- Interactive Scripts -->
    <script>
        // Mobile Menu Toggle
        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        }

        // Timeline Category Filter
        function filterTimeline(category) {
            const buttons = document.querySelectorAll('.tl-btn');
            buttons.forEach(btn => {
                btn.classList.remove('bg-brand-red', 'text-white', 'border-brand-red');
                btn.classList.add('bg-brand-card', 'text-gray-300', 'border-brand-border');
            });

            event.currentTarget.classList.remove('bg-brand-card', 'text-gray-300', 'border-brand-border');
            event.currentTarget.classList.add('bg-brand-red', 'text-white', 'border-brand-red');

            const items = document.querySelectorAll('.tl-item');
            items.forEach(item => {
                if (category === 'all' || item.getAttribute('data-category') === category) {
                    item.style.display = 'block';
                } else {
                    item.style.display = 'none';
                }
            });
        }

        // Philosophy Tabs Switcher
        function switchTab(tabKey) {
            const tabs = ['ontologi', 'epistemologi', 'aksiologi'];
            tabs.forEach(t => {
                const btn = document.getElementById(`tab-${t}`);
                const content = document.getElementById(`content-${t}`);
                if (t === tabKey) {
                    btn.classList.add('border-brand-red', 'text-white');
                    btn.classList.remove('border-transparent', 'text-gray-400');
                    content.classList.remove('hidden');
                    content.classList.add('block');
                } else {
                    btn.classList.remove('border-brand-red', 'text-white');
                    btn.classList.add('border-transparent', 'text-gray-400');
                    content.classList.add('hidden');
                    content.classList.remove('block');
                }
            });
        }

        // Lightbox Modal
        function openLightbox(src, caption) {
            document.getElementById('lightbox-img').src = src;
            document.getElementById('lightbox-caption').innerText = caption;
            document.getElementById('lightbox-modal').classList.remove('hidden');
        }

        function closeLightbox() {
            document.getElementById('lightbox-modal').classList.add('hidden');
        }

        // Search Modal functionality
        function toggleSearchModal() {
            const modal = document.getElementById('search-modal');
            modal.classList.toggle('hidden');
            modal.classList.toggle('flex');
            if(!modal.classList.contains('hidden')){
                document.getElementById('search-input').focus();
            }
        }

        const historyDatabase = [
            { title: "Tragedi Trisakti 12 Mei 1998", link: "#kronologi", snippet: "Penembakan 4 mahasiswa Universitas Trisakti oleh aparat keamanan." },
            { title: "Kerusuhan Massal 13-15 Mei", link: "#kronologi", snippet: "Penjarahan, pembakaran toko, dan tindakan rasial meluas di Jakarta." },
            { title: "Pengudayaan Gedung DPR 16-19 Mei", link: "#kronologi", snippet: "Puluhan ribu mahasiswa berkemah di Kompleks Senayan DPR/MPR." },
            { title: "Ketegangan Monas 20 Mei", link: "#kronologi", snippet: "Barikade militer jelang peringatan Hari Kebangkitan Nasional." },
            { title: "Soeharto Mundur 21 Mei 1998", link: "#kronologi", snippet: "Soeharto lengser setelah 32 tahun, BJ Habibie menjadi Presiden." },
            { title: "Latar Belakang Krisis Ekonomi", link: "#latar-belakang", snippet: "Anjloknya nilai tukar Rupiah dan krismon Asia 1997." },
            { title: "UU No. 9 Tahun 1998", link: "#era-reformasi", snippet: "Kemerdekaan menyampaikan pendapat di muka umum." },
            { title: "Kajian Filsafat Mei 1998", link: "#filsafat", snippet: "Ontologi, Epistemologi, dan Aksiologi peristiwa Mei 1998." }
        ];

        function performSearch() {
            const query = document.getElementById('search-input').value.toLowerCase().trim();
            const resultsContainer = document.getElementById('search-results');
            resultsContainer.innerHTML = '';

            if (query === '') return;

            const matches = historyDatabase.filter(item => 
                item.title.toLowerCase().includes(query) || item.snippet.toLowerCase().includes(query)
            );

            if (matches.length === 0) {
                resultsContainer.innerHTML = '<p class="text-gray-400 py-2">Tidak ditemukan hasil pencarian.</p>';
                return;
            }

            matches.forEach(item => {
                const div = document.createElement('div');
                div.className = 'p-2.5 bg-brand-black hover:bg-brand-border rounded-lg border border-brand-border cursor-pointer transition-colors';
                div.innerHTML = `<a href="${item.link}" onclick="toggleSearchModal()"><strong class="text-brand-brightred block">${item.title}</strong><span class="text-gray-300 text-[11px]">${item.snippet}</span></a>`;
                resultsContainer.appendChild(div);
            });
        }
    </script>
</body>
</html>
