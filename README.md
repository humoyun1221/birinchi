# birinchi
from confikk import dp
from aiogram.types import Message
from repleybatn import start_btn
from aiogram import executor


@dp.message_handler(commands=['start', 'help'])
async def start(msg: Message):
    # image = open('rasmlar/start.jpg', 'rb')
    text = f"single botiga xush kelibsiz."
    await msg.answer(text,reply_markup=start_btn)


@dp.message_handler(text='Badiiy Kitoblar📚')
async def badiy(msg: Message):
    tt = f"1.vijdon Azobi\n2.Benjimin franklin tarjimai holi\n3.Abu nasr Farobiy - fozil odamlar shaxri\n4.Jumali\n5.yaxshi ota\n6.boy ota kambagal ota\n7.Atom odatlar\n"
    await msg.answer_document(open('kitoblar/Amina Shanliko\'g\'li. Vijdon azobi (qissa).pdf','rb'))

@dp.message_handler(text='Tarixiy kitoblar📚')
async def tarixiy(msg: Message):
    tt = f"1.vijdon Azobi\n2.Benjimin franklin tarjimai holi\n3.Abu nasr Farobiy - fozil odamlar shaxri\n4.Jumali\n5.yaxshi ota\n6.boy ota kambagal ota\n7.Atom odatlar\n"
    await msg.answer_document(open('kitoblar/Amir Temur va Temuriylar davri tarixiy geografiyasi.doc','rb'))

@dp.message_handler(text='Diniy kitoblar📚')
async def diniy(msg: Message):
    tt = f"1.vijdon Azobi\n2.Benjimin franklin tarjimai holi\n3.Abu nasr Farobiy - fozil odamlar shaxri\n4.Jumali\n5.yaxshi ota\n6.boy ota kambagal ota\n7.Atom odatlar\n"
    await msg.answer_document(open('kitoblar/Diniy ekstremizm va terrorizm.pdf','rb'))

@dp.message_handler(text='Xalq ogzaki ijodi kitoblar📚')
async def xalq(msg: Message):
        tt = f"1.vijdon Azobi\n2.Benjimin franklin tarjimai holi\n3.Abu nasr Farobiy - fozil odamlar shaxri\n4.Jumali\n5.yaxshi ota\n6.boy ota kambagal ota\n7.Atom odatlar\n"
        await msg.answer_document(open('kitoblar//Shavkat_Mirziyoyev_Buyuk_kelajagimizni_mard_va_olijanob_xalqimiz.pdf', 'rb'))

if __name__ == "__main__":
    executor.start_polling(dp)
