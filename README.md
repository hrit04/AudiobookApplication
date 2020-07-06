# AudiobookApplication
import pyttsx3
import PyPDF2
#import pdftotext
book = open('C:/Users/Hritam/Desktop/AudioBook/ebook-v3.pdf', 'rb')
pdfReader = PyPDF2.PdfFileReader(book)
pages = pdfReader.numPages
print(pages)
speaker = pyttsx3.init()
speaker.say('Heyy human....! I am here to help you by reading any kind of book')
page = pdfReader.getPage(65)
text = page.extractText()
speaker.say(text)
speaker.runAndWait()
