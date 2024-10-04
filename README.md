from fpdf import FPDF

# Create a PDF document
pdf = FPDF()
pdf.add_page()

# Set title
pdf.set_font("Arial", 'B', 16)
pdf.cell(0, 10, 'Rangkuman Natural Language dan Machine Language', ln=True, align='C')

# Add Natural Language section
pdf.set_font("Arial", 'B', 14)
pdf.cell(0, 10, '1. Natural Language (Bahasa Alami)', ln=True)

pdf.set_font("Arial", '', 12)
natural_language_content = (
    "Definisi: Natural language adalah bahasa yang digunakan oleh manusia sehari-hari, "
    "seperti bahasa Indonesia, Inggris, dan lainnya. Bahasa ini bersifat ambigu, memiliki "
    "banyak aturan yang berubah-ubah, dan dapat dipengaruhi oleh budaya, intonasi, serta konteks.\n\n"
    "Karakteristik:\n"
    "- Bersifat fleksibel dan dinamis.\n"
    "- Memiliki struktur sintaksis yang kompleks.\n"
    "- Dapat ditafsirkan secara berbeda tergantung pada konteks dan budaya.\n"
    "- Contoh: Bahasa Indonesia, Inggris, Spanyol."
)
pdf.multi_cell(0, 10, natural_language_content)

# Add Machine Language section
pdf.set_font("Arial", 'B', 14)
pdf.cell(0, 10, '2. Machine Language (Bahasa Mesin)', ln=True)

pdf.set_font("Arial", '', 12)
machine_language_content = (
    "Definisi: Machine language adalah bahasa tingkat rendah yang dipahami langsung oleh komputer. "
    "Ini terdiri dari instruksi biner (0 dan 1) yang dijalankan oleh prosesor.\n\n"
    "Karakteristik:\n"
    "- Berupa kode-kode biner.\n"
    "- Sangat spesifik dan tidak ambigu.\n"
    "- Berhubungan langsung dengan perangkat keras komputer.\n"
    "- Tidak dapat dibaca atau dipahami secara langsung oleh manusia tanpa bantuan alat atau penerjemah.\n"
    "- Contoh: 10101001 (instruksi biner untuk prosesor)."
)
pdf.multi_cell(0, 10, machine_language_content)

# Add Case Study section
pdf.set_font("Arial", 'B', 14)
pdf.cell(0, 10, '3. Studi Kasus', ln=True)

pdf.set_font("Arial", '', 12)
case_study_content = (
    "1. Studi Kasus Natural Language Processing (NLP):\n"
    "- Latar Belakang: Dalam dunia teknologi, penggunaan bahasa alami sering dimanfaatkan "
    "dalam sistem seperti asisten virtual (misalnya, Siri, Google Assistant). "
    "Untuk itu, NLP digunakan agar mesin dapat memahami, menganalisis, dan menghasilkan "
    "teks atau ucapan dalam bahasa manusia.\n"
    "- Masalah: Tantangan utama dalam NLP adalah ambiguitas bahasa dan konteks yang bisa bervariasi.\n"
    "- Solusi: NLP memanfaatkan algoritma pembelajaran mesin, deep learning, serta basis data "
    "bahasa yang besar agar komputer dapat memahami konteks dan maksud dari bahasa manusia.\n"
    "- Contoh Implementasi: Google Translate menggunakan NLP untuk menerjemahkan antar bahasa "
    "dengan lebih baik dari waktu ke waktu, berdasarkan pembelajaran dari banyak data teks.\n\n"
    
    "2. Studi Kasus Machine Language dalam Sistem Tertanam (Embedded Systems):\n"
    "- Latar Belakang: Pada perangkat seperti microwave atau alat medis yang bekerja secara otomatis, "
    "bahasa mesin digunakan untuk memberikan instruksi langsung kepada perangkat keras.\n"
    "- Masalah: Bahasa mesin sangat sulit dipahami oleh manusia dan rentan terhadap kesalahan "
    "jika tidak diprogram dengan baik.\n"
    "- Solusi: Menggunakan bahasa assembly yang lebih mudah dipahami oleh manusia tetapi tetap "
    "bisa diterjemahkan ke dalam bahasa mesin oleh assembler.\n"
    "- Contoh Implementasi: Sistem kontrol otomotif menggunakan bahasa mesin untuk memastikan "
    "bahwa instruksi kecepatan, pengereman, dan stabilitas di eksekusi secara real-time oleh prosesor dalam kendaraan."
)
pdf.multi_cell(0, 10, case_study_content)

# Save the PDF to a file
pdf_file_path = '/mnt/data/rangkuman_natural_machine_language.pdf'
pdf.output(pdf_file_path)

pdf_file_path
