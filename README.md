import streamlit as st

st.title("📚 Database English Training Portal")

# 1. قسم القراءة (Reading Section)
st.header("1. Reading Challenge: What is a Primary Key?")
text = """
A Primary Key is a special relational database table column 
designated to uniquely identify all table records. It must contain 
unique values and cannot contain NULL values.
"""
st.info(text)

# سؤال لاختبار الفهم القرائي
question = "Based on the text, can a Primary Key have a NULL value?"
options = ["Yes, sometimes", "No, never", "Only in NoSQL"]
user_answer = st.radio(question, options)

if st.button("Check Reading Answer"):
    if user_answer == "No, never":
        st.success("Correct! Your reading comprehension is great. 🎉")
    else:
        st.error("Try again. Look closely at the last sentence.")

---
# 2. قسم التحدث (Speaking Section)
st.header("2. Speaking Challenge: Explain it!")
st.write("Click 'Record' and say the following sentence out loud:")
st.code("In SQL, the SELECT statement is used to fetch data.")

# هنا يمكنك دمج كود لتسجيل الصوت ومعالجته ببايثون
if st.button("🎤 Record & Analyze Voice"):
    st.warning("Voice analysis feature starting... (Connect your Speech-to-Text library here)")

# Streamlit Demo App

For video tutorial: [Streamlit: The Fastest Way To Build Python Apps?](https://www.youtube.com/watch?v=D0D4Pa22iG0&lc=Ugz_mHQgRHlnn1BJqlx4AaABAg)
