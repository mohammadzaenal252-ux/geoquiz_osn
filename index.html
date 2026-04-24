<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GeoQuiz OSN - Bank Soal Lengkap Puspresnas</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;700;800&display=swap');
        body { font-family: 'Plus Jakarta Sans', sans-serif; }
        .option-card { transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1); }
        .fade-in { animation: fadeIn 0.4s ease-out; }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .category-card:hover { transform: scale(1.02); }
    </style>
</head>
<body class="bg-slate-50 min-h-screen text-slate-900">

    <!-- Header / Navbar -->
    <header class="bg-blue-800 text-white shadow-xl p-5 sticky top-0 z-50 border-b-4 border-yellow-400">
        <div class="max-w-5xl mx-auto flex justify-between items-center">
            <div class="cursor-pointer" onclick="location.reload()">
                <h1 class="text-xl font-extrabold italic tracking-tighter uppercase">GEOQUIZ <span class="text-yellow-300">OSN</span></h1>
                <p class="text-[10px] opacity-80 font-bold uppercase tracking-widest text-blue-100">Simulasi Berbasis PDF Puspresnas</p>
            </div>
            <div id="active-category-indicator" class="hidden bg-blue-900 px-4 py-1.5 rounded-full text-xs font-bold border border-blue-700">
                Mode Latihan
            </div>
        </div>
    </header>

    <main class="max-w-5xl mx-auto px-4 py-8">
        
        <!-- Welcome Screen -->
        <div id="welcome-screen" class="fade-in">
            <div class="text-center mb-10">
                <h2 class="text-3xl font-black text-slate-800 mb-2">Pilih Materi Latihan</h2>
                <p class="text-slate-500 italic">Data diambil dari Bank Soal Puspresnas (Geologi, Iklim, Bencana, dll)</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6" id="category-list">
                <!-- Diisi otomatis oleh JavaScript -->
            </div>
        </div>

        <!-- Quiz Screen -->
        <div id="quiz-screen" class="hidden fade-in">
            <div class="flex justify-between items-center mb-6">
                <button onclick="confirmExit()" class="text-slate-400 hover:text-red-500 font-bold text-sm flex items-center gap-2 transition-colors">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 19l-7-7m0 0l7-7m-7 7h18" /></svg>
                    Keluar
                </button>
                <div class="flex items-center gap-4">
                    <span id="progress-text" class="text-[10px] font-black uppercase tracking-widest text-blue-600 bg-blue-50 px-3 py-1 rounded-full">Soal 1/5</span>
                    <div class="bg-white px-4 py-1.5 rounded-lg shadow-sm border border-slate-100 font-mono font-bold text-slate-600" id="timer">00:00</div>
                </div>
            </div>
            
            <div class="bg-white rounded-3xl shadow-xl p-8 border border-slate-100 mb-8 min-h-[400px] flex flex-col justify-center">
                <div id="question-text" class="text-lg md:text-xl font-bold text-slate-800 leading-relaxed mb-10">
                    Memuat pertanyaan...
                </div>
                <div id="options-container" class="grid grid-cols-1 gap-4"></div>
            </div>

            <div class="text-right">
                <button id="next-btn" disabled onclick="nextQuestion()" class="bg-slate-200 text-slate-400 px-10 py-4 rounded-2xl font-black uppercase tracking-wider text-sm transition-all shadow-md">
                    Lanjut
                </button>
            </div>
        </div>

        <!-- Result Screen -->
        <div id="result-screen" class="hidden fade-in pb-20">
            <div class="bg-white rounded-3xl shadow-2xl p-8 border border-slate-100 text-center mb-8">
                <h2 class="text-2xl font-black text-slate-800 mb-6 uppercase italic">Analisis Hasil</h2>
                <div class="flex justify-center gap-4 mb-8">
                    <div class="bg-blue-600 p-6 rounded-2xl text-white min-w-[120px]">
                        <div id="final-score" class="text-4xl font-black">0</div>
                        <div class="text-[10px] font-bold uppercase opacity-80">Skor Akhir</div>
                    </div>
                    <div class="bg-emerald-500 p-6 rounded-2xl text-white min-w-[120px]">
                        <div id="correct-count" class="text-4xl font-black">0</div>
                        <div class="text-[10px] font-bold uppercase opacity-80">Benar</div>
                    </div>
                </div>
                <button onclick="location.reload()" class="bg-slate-800 text-white px-8 py-3 rounded-xl font-bold hover:bg-black transition-all">Selesai & Menu Utama</button>
            </div>

            <div class="space-y-4">
                <h3 class="font-black text-slate-700 uppercase tracking-widest text-sm ml-2">Detail Pembahasan (Sesuai PDF)</h3>
                <div id="review-section" class="space-y-4"></div>
            </div>
        </div>
    </main>

    <script>
        const quizData = {
            "iklim": {
                title: "Iklim & Perubahan Iklim",
                icon: "M3 15a4 4 0 110-8 4 4 0 010 8z M15 8V7a3 3 0 00-3-3h-1m-4 10V15a3 3 0 013-3h1",
                questions: [
                    { tanya: "Aktivitas pembakaran bahan bakar fosil dan penebangan hutan memengaruhi perubahan iklim dengan cara...", opsi: ["Membantu meningkatkan kadar oksigen di udara", "Membuat gas rumah kaca di atmosfer berkurang", "Menambah jumlah CO2 sehingga memperkuat efek rumah kaca", "Menjadikan pola cuaca dunia semakin stabil", "Mempercepat proses fotosintesis di lautan"], kunci: 2, bahas: "Pembakaran fosil melepaskan CO2, sementara penebangan hutan menghilangkan penyerap karbon alami. Hal ini memperkuat efek 'selimut' di atmosfer." },
                    { tanya: "Peningkatan kadar CO2 di laut akan memengaruhi kondisi fisiologis terumbu karang dalam bentuk...", opsi: ["Pertumbuhan karang jadi lebih cepat", "Pemutihan (bleaching) karena suhu air laut naik", "Menambah jumlah ikan di terumbu karang", "Mengurangi kadar oksigen secara drastis", "Memperkuat struktur kalsium karang"], kunci: 1, bahas: "Suhu panas menyebabkan stres pada karang sehingga mengeluarkan alga simbiotik (Zooxanthellae) yang memberi warna, menyebabkan pemutihan." },
                    { tanya: "Target utama Paris Agreement yang disepakati lebih dari 190 negara adalah menahan kenaikan suhu global di bawah...", opsi: ["1,0°C", "1,5°C", "2,0°C", "2,5°C", "3,0°C"], kunci: 1, bahas: "Paris Agreement menargetkan penahanan suhu global agar tidak melewati ambang batas 1,5 derajat Celcius untuk mencegah bencana iklim." }
                ]
            },
            "geologi": {
                title: "Geologi & Geomorfologi",
                icon: "M20 7l-8-4-8 4m16 0l-8 4m8-4v10l-8 4m0-10L4 7m8 4v10M4 7v10l8 4",
                questions: [
                    { tanya: "Palung Mariana terbentuk karena Lempeng Pasifik...", opsi: ["Naik ke atas Lempeng Filipina", "Naik ke atas Lempeng Indo-Australia", "Menunjam ke bawah Lempeng Filipina", "Menunjam ke bawah Lempeng Indo-Australia", "Menunjam ke bawah Lempeng Eurasia"], kunci: 2, bahas: "Lempeng Samudra (SiMa) yang lebih berat menunjam ke bawah lempeng yang lebih ringan (Subduksi) membentuk palung." },
                    { tanya: "Lempeng Samudra (SiMa) lebih berat daripada Lempeng Benua (SiAl) karena mengandung banyak...", opsi: ["Alumunium", "Magnesium", "Kalsium", "Tembaga", "Perak"], kunci: 1, bahas: "SiMa (Silikat Magnesium) memiliki densitas lebih tinggi daripada SiAl (Silikat Alumunium)." },
                    { tanya: "Morfologi sungai yang berkelok-kelok tajam secara teratur melalui dataran banjir disebut...", opsi: ["Anastomosing", "Braided River", "Sungai Kelok Banyak", "Meandering", "Sungai U"], kunci: 3, bahas: "Meandering terbentuk karena proses erosi dan sedimentasi yang berkelanjutan pada dataran rendah." },
                    { tanya: "Lingkungan pengendapan di ujung sungai tempat sungai masuk ke laut disebut...", opsi: ["Dataran Banjir", "Anak Sungai", "Daerah Aliran Sungai", "Delta", "Spit"], kunci: 3, bahas: "Delta terbentuk saat kecepatan aliran sungai menurun drastis di muara sehingga sedimen mengendap." }
                ]
            },
            "bencana": {
                title: "Manajemen Bencana",
                icon: "M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z",
                questions: [
                    { tanya: "Tipe gerakan tanah dengan kejenuhan air paling tinggi (paling basah) adalah...", opsi: ["Soil Creep", "Slump", "Mudflow", "Rockfall", "Topples"], kunci: 2, bahas: "Mudflow (aliran lumpur) memiliki kadar air sangat tinggi sehingga material mengalir seperti cairan kental." },
                    { tanya: "Fenomena tanah kehilangan kekuatan dan berubah seperti cairan akibat guncangan gempa disebut...", opsi: ["Erosi", "Likuifaksi", "Abrasi", "Subsiden", "Deflasi"], kunci: 1, bahas: "Likuifaksi terjadi pada tanah berpasir jenuh air saat terkena guncangan hebat (misal: Gempa Palu)." },
                    { tanya: "Unsur kapasitas finansial dalam mitigasi bencana ditunjukkan oleh...", opsi: ["EWS", "Peta Risiko", "Akses terhadap dana pinjaman mitigasi", "Kurikulum Sekolah", "Rencana Darurat"], kunci: 2, bahas: "Kapasitas finansial berkaitan dengan ketersediaan dana darurat, asuransi, atau akses modal pemulihan." }
                ]
            },
            "sumberdaya": {
                title: "Sumber Daya Alam",
                icon: "M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h14a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z",
                questions: [
                    { tanya: "Pasangan sumber daya alam renewable dan non-renewable yang tepat adalah...", opsi: ["Nuklir; Minyak Bumi", "Surya; Panas Bumi", "Gas Alam; Air", "Angin; Gas Alam", "Biomassa; Panas Bumi"], kunci: 3, bahas: "Angin dapat diperbaharui, sementara Gas Alam adalah energi fosil yang akan habis." },
                    { tanya: "Rasio elektrifikasi adalah...", opsi: ["Jumlah daya listrik nasional", "Persentase rumah tangga dengan akses listrik", "Jumlah gardu listrik daerah", "Biaya tagihan rata-rata", "Produksi batubara PLTU"], kunci: 1, bahas: "Rasio ini mengukur sejauh mana pemerataan akses listrik menjangkau seluruh penduduk di suatu wilayah." },
                    { tanya: "Faktor fisik lokasi yang paling ideal untuk PLTA adalah...", opsi: ["Topografi datar", "Curah hujan rendah", "Topografi curam & curah hujan tinggi", "Dekat pusat kota saja", "Pengaruh musim hujan saja"], kunci: 2, bahas: "PLTA butuh beda tinggi (topografi curam) dan debit air yang stabil (curah hujan tinggi)." }
                ]
            },
            "lingkungan": {
                title: "Lingkungan & Pembangunan",
                icon: "M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z",
                questions: [
                    { tanya: "Kadar kontaminasi Kadmium (Cd) sebesar 200 ppm berarti...", opsi: ["200 kali ambang batas", "200 ml dalam 1000 mg", "200 mg dalam 1 ml", "200 gram dalam 1 liter", "200 mg dalam 1000 ml (1 liter)"], kunci: 4, bahas: "1 ppm (Part Per Million) setara dengan 1 mg zat terlarut dalam 1 liter (1000 ml) air." },
                    { tanya: "Skenario masa depan di mana ketimpangan ekstrem menyebabkan kaum kaya memagari diri dengan militer sementara luar benteng kacau disebut...", opsi: ["Market Forces", "Eco-communalism", "Fortress World", "Great Transitions", "Balanced Growth"], kunci: 2, bahas: "Fortress World adalah skenario distopia di mana pembangunan gagal mencapai keadilan sosial." },
                    { tanya: "Skenario Market Forces menganggap masalah lingkungan akan selesai sendiri melalui...", opsi: ["Hukum adat", "Pertanian tradisional", "Teknologi dan mekanisme pasar", "Pemerataan populasi", "Pengurangan konsumsi"], kunci: 2, bahas: "Market Forces fokus pada pertumbuhan GDP dan percaya pasar akan mengoreksi diri sendiri." }
                ]
            },
            "pertanian": {
                title: "Pertanian & Pangan",
                icon: "M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253",
                questions: [
                    { tanya: "Perbedaan signifikan antara Revolusi Hijau dan Revolusi Industri 4.0 adalah...", opsi: ["Hanya 4.0 yang meningkatkan produksi", "Revolusi Hijau meningkatkan produksi tapi berdampak lingkungan signifikan", "4.0 tidak menggunakan AI", "Hijau lebih efisien teknologi", "Keduanya tidak ada hubungan"], kunci: 1, bahas: "Revolusi Hijau fokus pada bibit unggul & kimia, sementara 4.0 fokus pada efisiensi lewat IoT/AI." },
                    { tanya: "Tantangan utama dari sistem pertanian sawah (lahan basah) adalah...", opsi: ["Minim tenaga kerja", "Ketergantungan irigasi & risiko kekeringan", "Pupuk kimia terlalu murah", "Kurang bibit padi", "Tidak bisa pakai traktor"], kunci: 1, bahas: "Sawah butuh genangan air mutlak; jika irigasi rusak atau kemarau panjang, risiko gagal panen (puso) sangat tinggi." },
                    { tanya: "Fenomena gagal panen padi yang biasanya disebabkan kekeringan atau hama masif disebut...", opsi: ["Fuso", "Erosi", "Likuifaksi", "Pencemaran", "Infiltrasi"], kunci: 0, bahas: "Puso adalah istilah untuk kondisi tanaman padi yang tidak menghasilkan bulir sama sekali." }
                ]
            }
        };

        let currentCategory = "";
        let currentQuestionIndex = 0;
        let userAnswers = [];
        let timerSeconds = 0;
        let timerInterval;

        function init() {
            const list = document.getElementById('category-list');
            list.innerHTML = '';
            for (let key in quizData) {
                const cat = quizData[key];
                const card = document.createElement('div');
                card.className = "category-card bg-white p-6 rounded-3xl shadow-md border border-slate-100 cursor-pointer hover:shadow-xl hover:border-blue-200 transition-all group";
                card.onclick = () => startQuiz(key);
                card.innerHTML = `
                    <div class="bg-blue-50 w-14 h-14 rounded-2xl flex items-center justify-center mb-4 group-hover:bg-blue-600 group-hover:text-white transition-colors text-blue-600">
                        <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="${cat.icon}"></path></svg>
                    </div>
                    <h3 class="text-lg font-bold text-slate-800">${cat.title}</h3>
                    <p class="text-xs text-slate-400 mt-1 font-semibold uppercase tracking-tight">${cat.questions.length} Soal Master</p>
                `;
                list.appendChild(card);
            }
        }

        function startQuiz(categoryKey) {
            currentCategory = categoryKey;
            currentQuestionIndex = 0;
            userAnswers = [];
            timerSeconds = 0;
            document.getElementById('welcome-screen').classList.add('hidden');
            document.getElementById('quiz-screen').classList.remove('hidden');
            document.getElementById('active-category-indicator').classList.remove('hidden');
            document.getElementById('active-category-indicator').innerText = quizData[categoryKey].title;
            startTimer();
            showQuestion();
        }

        function startTimer() {
            if(timerInterval) clearInterval(timerInterval);
            timerInterval = setInterval(() => {
                timerSeconds++;
                const m = Math.floor(timerSeconds / 60).toString().padStart(2, '0');
                const s = (timerSeconds % 60).toString().padStart(2, '0');
                document.getElementById('timer').innerText = `${m}:${s}`;
            }, 1000);
        }

        function showQuestion() {
            const q = quizData[currentCategory].questions[currentQuestionIndex];
            const total = quizData[currentCategory].questions.length;
            document.getElementById('progress-text').innerText = `Soal ${currentQuestionIndex + 1} / ${total}`;
            document.getElementById('question-text').innerText = q.tanya;
            
            const container = document.getElementById('options-container');
            container.innerHTML = '';
            
            q.opsi.forEach((opt, idx) => {
                const btn = document.createElement('button');
                btn.className = "option-card w-full text-left p-5 rounded-2xl border-2 border-slate-100 hover:border-blue-200 hover:bg-blue-50 font-semibold text-slate-700 flex items-center gap-4 group";
                btn.innerHTML = `
                    <span class="w-10 h-10 flex-shrink-0 flex items-center justify-center rounded-xl bg-slate-50 text-slate-400 font-black group-hover:bg-blue-600 group-hover:text-white transition-all">${String.fromCharCode(65 + idx)}</span>
                    <span class="text-sm md:text-base">${opt}</span>
                `;
                btn.onclick = () => selectOption(idx);
                container.appendChild(btn);
            });
            
            document.getElementById('next-btn').disabled = true;
            document.getElementById('next-btn').className = "bg-slate-200 text-slate-400 px-10 py-4 rounded-2xl font-black uppercase tracking-wider text-sm cursor-not-allowed transition-all";
        }

        function selectOption(idx) {
            userAnswers[currentQuestionIndex] = idx;
            const cards = document.querySelectorAll('.option-card');
            cards.forEach((card, i) => {
                const badge = card.querySelector('span:first-child');
                if(i === idx) {
                    card.classList.add('border-blue-600', 'bg-blue-50');
                    badge.classList.add('bg-blue-600', 'text-white');
                } else {
                    card.classList.remove('border-blue-600', 'bg-blue-50');
                    badge.classList.remove('bg-blue-600', 'text-white');
                }
            });
            
            const nextBtn = document.getElementById('next-btn');
            nextBtn.disabled = false;
            nextBtn.className = "bg-blue-600 text-white px-10 py-4 rounded-2xl font-black uppercase tracking-wider text-sm hover:bg-blue-700 shadow-lg cursor-pointer transition-all";
            nextBtn.innerText = currentQuestionIndex === quizData[currentCategory].questions.length - 1 ? "Selesaikan Latihan" : "Lanjut";
        }

        function nextQuestion() {
            if (currentQuestionIndex < quizData[currentCategory].questions.length - 1) {
                currentQuestionIndex++;
                showQuestion();
            } else {
                showResults();
            }
        }

        function showResults() {
            clearInterval(timerInterval);
            document.getElementById('quiz-screen').classList.add('hidden');
            document.getElementById('result-screen').classList.remove('hidden');
            document.getElementById('active-category-indicator').classList.add('hidden');
            
            const questions = quizData[currentCategory].questions;
            let correct = 0;
            const review = document.getElementById('review-section');
            review.innerHTML = '';
            
            questions.forEach((q, i) => {
                const isCorrect = userAnswers[i] === q.kunci;
                if(isCorrect) correct++;
                
                const card = document.createElement('div');
                card.className = `p-6 rounded-3xl border fade-in ${isCorrect ? 'bg-emerald-50 border-emerald-100' : 'bg-red-50 border-red-100'}`;
                card.innerHTML = `
                    <p class="font-bold text-slate-800 mb-3">${q.tanya}</p>
                    <div class="text-sm mb-4">
                        <div class="flex items-center gap-2 mb-1">
                            <span class="font-bold text-slate-500">Pilihan:</span>
                            <span class="${isCorrect ? 'text-emerald-700 font-bold' : 'text-red-700 font-bold'}">${q.opsi[userAnswers[i]] || 'Tidak Dijawab'}</span>
                        </div>
                        ${!isCorrect ? `
                        <div class="flex items-center gap-2">
                            <span class="font-bold text-slate-500">Kunci:</span>
                            <span class="text-blue-700 font-bold italic">${q.opsi[q.kunci]}</span>
                        </div>` : ''}
                    </div>
                    <div class="bg-white/60 p-4 rounded-xl text-xs text-slate-600 border border-slate-100 leading-relaxed">
                        <strong class="uppercase text-[9px] tracking-widest text-slate-400 block mb-1">Analisis Geografi:</strong> ${q.bahas}
                    </div>
                `;
                review.appendChild(card);
            });
            
            document.getElementById('final-score').innerText = Math.round((correct / questions.length) * 100);
            document.getElementById('correct-count').innerText = `${correct}/${questions.length}`;
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function confirmExit() { 
            if(confirm("Yakin ingin keluar? Progres latihanmu akan hilang.")) location.reload(); 
        }

        // Jalankan inisialisasi
        init();
    </script>
</body>
</html>
