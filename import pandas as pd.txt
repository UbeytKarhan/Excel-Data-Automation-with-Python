import pandas as pd

# Excel dosyasını oku
df = pd.read_excel("data.xlsx")

# Boş satırları sil
df = df.dropna()

# Tekrarlayan verileri sil
df = df.drop_duplicates()

# Yeni dosyaya kaydet
df.to_excel("cleaned_data.xlsx", index=False)

print("Data cleaned successfully!")