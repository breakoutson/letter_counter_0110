import re
import streamlit as st

st.title("BREAKOUT SON")

# 블로그 에디터 창에서 안보이지만 따라오는 단어들
remove_list = ['대표사진 삭제', '사진 설명을 입력하세요.', '출처 입력', '사진 삭제','이미지 썸네일 삭제', '동영상 정보 상세 보기','동영상 설명을 입력하세요.']

# 줄바꿈 있는 본문 입력
# str = pyautogui.prompt()
str = st.text_input('본문 입력')

# 따라온 단어들 삭제
for i in remove_list:
    str = str.replace(i, '')

# 공백과 줄바꿈 삭제
str_re = re.sub('\n| ', '', str)

print (str_re)
print ('=======================================')
print ('공백제외:', len(str_re), '|', '공백포함:', len(str),'자 입니다')

import time
with st.spinner('Wait for it...'):
    time.sleep(1)
st.success('Done!')

st.write('### 공백 제외', len(str_re),'자, 공백 포함', len(str),'자 입니다')
st.info(str_re)
