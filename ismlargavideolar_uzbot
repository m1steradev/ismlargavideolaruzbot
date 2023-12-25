<?php
//Dasturchi @RAXMONOV_Y1
//MANBA BILAN OLING!

ob_start();
define("API_KEY","API TOKEN"); //BU YERGA BOT TOKENI
$admin = "admin id";

function bot($method,$datas=[]){
    $url = "https://api.telegram.org/bot".API_KEY. "/" . $method;
    $ch = curl_init();
    curl_setopt($ch, CURLOPT_URL, $url);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_setopt($ch, CURLOPT_POSTFIELDS, $datas);
    $res = curl_exec($ch);

    if(curl_error($ch)){
        var_dump(curl_error($ch));
    }else{
        return json_decode($res);
    }
}

$update = json_decode(file_get_contents("php://input"));
$message = $update->message;
$chat_id = $message->chat->id;
$messaga_id = $message->message_id;
$username = $message->from->username;
$uid = $message->from->id;
$ism = $message->from->first_name;
$familya = $message->from->last_name;
$name = "<a href='tg://user?id=$uid'>$ism $familya</a>";
$text = $message->text;
$type = $message->chat->type;
$sana1 = date('d.m.Y');
$time=date('H:i:s',strtotime('0 hour'));
$adminuser="@mr_adev";
$botuser="@ismlargavideolar_uzbot";
$opened="2023-yil 20-may soat 15:18 da";
$ulink="https://t.me/share/url?text=%20Bu%20botga%20sizni%20ham%20taklif%20etaman!%20O'zingiz%20uchun%20ajoyib%20videolar%20yasab%20oling✅%0A%0A👉%20@iismlargavideolar_uzbot%20🎁";
$reklama="Bu yerda 🫵sizning reklamangiz bo‘lishi mumkin edi, kechqolmadiz reklama bo‘yicha: 🤵‍♂-> $adminuser ga yozing"; 
$reklama2="<a href='https://t.me/mradevportfolio'><b> KANALIMIZ </b> </a>";
$idi = $message->from->id;
if(!file_exists('steep.txt')){
  fopen('steep.txt','wr');
}

$xabar = $update->message;
$xabar_id = $xabar->message_id;

$step = file_get_contents('steep.txt');
$step2 = file_get_contents("step/$chat_id.step");

mkdir("step");
mkdir("step/$chat_id");
mkdir("stat");
mkdir("ism");

$sana = date('d-M Y',strtotime('2 hour'));
$oy_nomi = date('F',strtotime('2 hour'));
$bu_oy = date('t',strtotime('2 hour'));
$bugungi_sana = date('d',strtotime('2 hour'));
$natija=$bugungi_sana+41;
$boldi="$natija kun bo‘ldi";

//inline method
$data = $update->callback_query->data;
$qid = $update->callback_query->id;
$id = $update->inline_query->id;
$query = $update->inline_query->query;
$query_id = $update->inline_query->from->id;
$cid2 = $update->callback_query->message->chat->id;
$mid2 = $update->callback_query->message->message_id;
$callfrid = $update->callback_query->from->id;
$callname = $update->callback_query->from->first_name;
$calluser = $update->callback_query->from->username;
$surname = $update->callback_query->from->last_name;
$about = $update->callback_query->from->about;
$nameuz = "<a href='tg://user?id=$callfrid'>$callname $surname</a>";
$back = "◀️ Orqaga";


mkdir("data");

$id = $message->from->id;
$username = $message->from->username;

$userlar = file_get_contents("stat/stat.txt");
$stat = substr_count($userlar, "n");
if(isset($message)){
   $baza = file_get_contents("stat/stat.txt");
   if(mb_stripos($baza,$chat_id) !==false){
   }else{
   $txt="n$chat_id";
   $file=fopen("stat/stat.txt","a");
   fwrite($file,$txt);
   fclose($file);
   }
}

function sendTypingIndicator($chat_id) {
    $typingIndicator = array(
      'chat_id' => $chat_id,
      'action' => 'typing',
  );

  bot('sendChatAction', $typingIndicator);
}

function sendMessageWithTyping($chat_id, $message) {
$typingDelay = 1; 
  sendTypingIndicator($chat_id);
  usleep($typingDelay * 1000);
  $mid = $message->message_id;
  bot('sendMessage', [
      'chat_id' => $chat_id,
      'text' => $message,
      'reply_to_message_id' =>$message,
  ]);
}

sendMessageWithTyping($chat_id, "");

if ($text == "/dasturchi"){
    bot('SendPhoto',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'photo'=>"https://t.me/ismlargavideolar_database/3",
        'caption'=>"🤵‍♂Ism:  Yaxyobek
🤵‍♂Familya:  Raxmonov 
🤵‍♂Yoshi: 18 yoshda
🤵‍♂Millati: Uyg‘ur va O‘zbek
🤵‍♂Yashash joyi: Andijon shahar
🤵‍♂Yo‘nalishi:  Dasturchi 
🤵‍♂Tillar:  Python, PHP
🤵‍♂Darajasi:  Junior 
🤵‍♂Sayti: waiting...
🤵‍♂Telegrami: @mr_adev",
    ]);
}

if ($text =="👨‍💻BOT DASTURCHISI"){
    bot('SendPhoto',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'photo'=>"https://t.me/ismlargavideolar_database/3",
        'caption'=>"🤵‍♂Ism:  Yaxyobek
🤵‍♂Familya:  Raxmonov 
🤵‍♂Yoshi: 18 yoshda
🤵‍♂Millati: Uyg‘ur va O‘zbek
🤵‍♂Yashash joyi: Andijon shahar
🤵‍♂Yo‘nalishi:  Dasturchi 
🤵‍♂Tillar:  Python, PHP
🤵‍♂Darajasi:  Junior 
🤵‍♂Sayti: waiting...
🤵‍♂Telegrami: @Raxmonov_Y1",
    ]);
}

$ulashish = json_encode([
                'inline_keyboard'=>[
[['text'=>"👥Do‘stlarga ulashish↪️",'url'=>"https://t.me/share/url?text=%20Bu%20botga%20sizni%20ham%20taklif%20etaman!%20O'zingiz%20uchun%20ajoyib%20videolar%20yasab%20oling✅%0A%0A👉%20@ismlargavideolar_uzbot%20🎁"]],
    ]
    ]);

$asosiy = json_encode([
    'resize_keyboard'=>true,
    'keyboard'=>[
  [['text'=>"📝 RASM BO‘LMI"]],[['text'=>"❤️‍🔥KO'ZGA HARF VIDEO👁"],['text'=>"🫶ISMLARGA SEVGI IZHOR VIDEO❤️‍🔥"]],[['text'=>"😍ISMLARGA VIDEOLAR🤗"],['text'=>"🥰HARFLARGA VIDEOLAR😎"]],[['text'=>"🌐FOYDALI BO‘LIM🌐"]],[['text'=>"👨‍💻BOT DASTURCHISI"]],
    ]
    ]);
    
    $rasm = json_encode([
    'resize_keyboard'=>true,
    'keyboard'=>[
  [['text'=>"🎉Tug‘ulgan kun tabrik"],['text'=>"❤️‍🔥Ismlarga rasmlar"]],[['text'=>"🟡Humans stilida ism🟡"],['text'=>"💕Paralik rasmlar💞"]],[['text'=> "📛Orqaga"]], 
    ]
    ]);
    
    
    if ($text == "📝 RASM BO‘LMI"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n kerakli bo‘limni tanlang👇",
        'reply_markup'=>$rasm, 
        ]); 
}

if ($text == "📛Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ ASOSIY MENYUDASIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇!",
        'reply_markup'=>$asosiy,
    ]);
}

    
    if($text=="/speed"){
$start_time = round(microtime(true) * 1000);
      $send=  bot('sendmessage', [
                'chat_id' => $chat_id, 
                'text' =>"Loading...",
            ])->result->message_id;

                    $end_time = round(microtime(true) * 1000);
                    $time_taken = $end_time - $start_time;
                    bot('editMessagetext',[
                        "chat_id" => $chat_id,
                        "message_id" => $send,
                        "text" => "$botuser botining tezligi👇🏻\n\n⚡️ Botning tezligi: " . $time_taken .  "Ms",
]);
}

if ($text == "🔙Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ ASOSIY MENYUDASIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇!",
        'reply_markup'=>$asosiy,
    ]);
}

if ($text =="ibrohim"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"$reklama2",
    ]);
}

$sevgi1 = json_encode([
                'resize_keyboard'=>true,
                'keyboard'=>[
[['text'=>"👧Qiz bola izhori"],['text'=>"👨O‘g‘il bola izhori"]],[['text'=>"🔙Orqaga"]],
    ]
    ]);

if ($text == "🫶ISMLARGA SEVGI IZHOR VIDEO❤️‍🔥"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZGA QAYSI BIRI KERAK👇!",
        'reply_markup'=>$sevgi1,
    ]);
}

$sevgi2 = json_encode([
                'resize_keyboard'=>true,
                'keyboard'=>[
[['text'=>"Asal🥰"],['text'=>"Iroda🥰"],['text'=>"Manzura🥰"],['text'=>"Mushtariy🥰"]],[['text'=>"Bonu🥰"],['text'=>"Durdona🥰"],['text'=>"Nigina🥰"],['text'=>"Shirina🥰"]],[['text'=>"Zuhra🥰"],['text'=>"Madina🥰"],['text'=>"Rayxon🥰"],['text'=>"Sevinch🥰"]],[['text'=>"Malika🥰"],['text'=>"Sarvinoz🥰"],['text'=>"Shaxnoza🥰"],['text'=>"Guli🥰"]],[['text'=>"👨Orqaga"]],
]
]);

if ($text == "👨Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ ASOSIY MENYUDASIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇!",
        'reply_markup'=>$sevgi1,
    ]);
}


if ($text == "👨O‘g‘il bola izhori"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\nMENYUDAN O‘ZINGIZGA KERAKLI ISMNI TANLANG👇!",
        'reply_markup'=>$sevgi2,
    ]);
}

if ($text == "Asal🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/47",
        'caption'=>"Asal❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "Bonu🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/36",
        'caption'=>"Bonu❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "Nigina🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/33",
        'caption'=>"Nigina❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "Guli🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/34",
        'caption'=>"Guli❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "Rayxon🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/35",
        'caption'=>"Rayxon❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "Durdona🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/37",
        'caption'=>"Durdona❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "Madina🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/38",
        'caption'=>"Madina❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "Zuhra🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/39",
        'caption'=>"Zuhra❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "Sevinch🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/40",
        'caption'=>"Sevinch❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "Malika🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/41",
        'caption'=>"Malika❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "Sarvinoz🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/42",
        'caption'=>"Sarvinoz❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "Shaxnoza🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/43",
        'caption'=>"Shaxnoza‍❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "Manzura🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/44",
        'caption'=>"Manzura❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "Mushtariy🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/45",
        'caption'=>"Mushtariy❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "Shirina🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/46",
        'caption'=>"Shirina❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "Iroda🥰"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/48",
        'caption'=>"Iroda❤️‍🔥 ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

$sevgi3 = json_encode([
    'resize_keyboard'=>true,
    'keyboard'=>[
        [['text'=>"❤️‍🔥Abdulbosit"],['text'=>"❤️‍🔥Adham"],['text'=>"❤️‍🔥Asadbek"],['text'=>"❤️‍🔥Asliddin"]],[['text'=>"❤️‍🔥Aziz"],['text'=>"❤️‍🔥Bekzod"],['text'=>"❤️‍🔥Dovudbek"],['text'=>"❤️‍🔥Eldor"]],[['text'=>"❤️‍🔥Farrux"],['text'=>"❤️‍🔥Komil"],['text'=>"❤️‍🔥Jaxongir"],['text'=>"❤️‍🔥Javohir"]],[['text'=>"❤️‍🔥Muhammad"],['text'=>"❤️‍🔥Nodirbek"],['text'=>"❤️‍🔥Izzat"],['text'=>"❤️‍🔥Sarvar"]],[['text'=>"❤️‍🔥Shaxriyor"],['text'=>"❤️‍🔥Shaxzod"],['text'=>" ❤️‍🔥Shohjahon"],['text'=>"❤️‍🔥Umid"]],[['text'=>"👧Orqaga "]]
    ]
    ]);

if ($text == "👧Orqaga"){
        bot('SendMessage',[
            'chat_id'=>$chat_id,
            'message_id'=>$messaga_id,
            'parse_mode'=>"html",
            'text'=>"Hurmatli $name,\n\n SIZ IZHORLAR MENYUSIDASIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇!",
            'reply_markup'=>$sevgi1,
        ]);
    }

// Qiz bola izhor video bo'limi

// 1-qator

if ($text == "👧Qiz bola izhori"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\nMENYUDAN O‘ZINGIZGA KERAKLI ISMNI TANLANG👇!",
        'reply_markup'=>$sevgi3,
    ]);
}

if ($text == "❤️‍🔥Abdulbosit"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/64",
        'caption'=>"❤️‍🔥Abdulbosit ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Adham"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/67",
        'caption'=>"❤️‍🔥Adham ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Asadbek"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/66",
        'caption'=>"❤️‍🔥Asadbek ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Asliddin"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/55",
        'caption'=>"❤️‍🔥Asliddin ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

// 2-qator 

if ($text == "❤️‍🔥Aziz"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/65",
        'caption'=>"❤️‍🔥Aziz ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Bekzod"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/63",
        'caption'=>"❤️‍🔥Bekzod ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Dovudbek"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/53",
        'caption'=>"❤️‍🔥Dovudbek ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Eldor"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/68",
        'caption'=>"❤️‍🔥Eldor ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

// 3-qator

if ($text == "❤️‍🔥Farrux"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/57",
        'caption'=>"❤️‍🔥Farrux ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Komil"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/49",
        'caption'=>"❤️‍🔥Komil ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Jaxongir"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/56",
        'caption'=>"❤️‍🔥Jaxongir ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Javohir"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/52",
        'caption'=>"❤️‍🔥Javohir ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

// 4-qator

if ($text == "❤️‍🔥Muhammad"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/51",
        'caption'=>"❤️‍🔥Muhammad ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Nodirbek"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/54",
        'caption'=>"❤️‍🔥Nodirbek ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Sarvar"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/58",
        'caption'=>"❤️‍🔥Sarvar ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Shaxzod"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>'html',
        'video'=>"https://t.me/ismlargavideolar_database/50",
        'caption'=>"❤️‍🔥Shaxzod ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Shaxriyor"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/59",
        'caption'=>"❤️‍🔥Shaxriyor ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Izzat"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/60",
        'caption'=>"❤️‍🔥Izzat ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Shohjahon"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/61",
        'caption'=>"❤️‍🔥Shohjahon ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🔥Umid"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/62",
        'caption'=>"❤️‍🔥Umid ismiga aytilgan sevgi izhor video tayyor✅

♾♾♾♾♾
🤖 @ismlargavideolar_uzbot tomonidan yasab berildi! 

❤️‍🔥Quyidagi menyudan boshqa ismlarga ham sevgi izhorlar yuklab saqlab oling👇",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "/start"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Salom🤝 $name sizni botimda ko'rib turganimdan xursandman!\n
pastdagi menyulardan o'zingizga kerakligini tanlab oling👇",
        'reply_markup'=>$asosiy,
    ]);
}

$kstil = json_encode([
   'resize_keyboard'=>true,
   'keyboard'=>[
   [['text'=>"👁BIRINCHI STIL👁"],['text'=>"👁IKKINCHI STIL👁"]],[['text'=>"👁Orqaga"]],
   ]
   ]);
   
  if ($text == "👁Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ ASOSIY MENYUGA QAYTDINGIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇",
        'reply_markup'=>$asosiy,
    ]);
}

$kozga = json_encode([
    'resize_keyboard'=>true,
    'keyboard'=>[
    [['text'=>"🫶A"],['text'=>"🫶B"],['text'=>"🫶D"],['text'=>"🫶E"],['text'=>"🫶F"]],[['text'=>"🫶G"],['text'=>"🫶H"],['text'=>"🫶I"],['text'=>"🫶J"],['text'=>"🫶K"]],[['text'=>"🫶L"],['text'=>"🫶M"],['text'=>"🫶N"],['text'=>"🫶O"],['text'=>"🫶P"]],[['text'=>"🫶Q"],['text'=>"🫶R"],['text'=>"🫶S"],['text'=>"🫶T"],['text'=>"🫶U"]],[['text'=>"🫶V"],['text'=>"🫶X"],['text'=>"🫶Y"],['text'=>"🫶Z"],['text'=>"🫶O'"]],[['text'=>"🫶G'"],['text'=>"🫶SH"],['text'=>"🫶CH"]],[['text'=>"🫶Orqaga"]],
    ]
    ]);

if ($text == "❤️‍🔥KO'ZGA HARF VIDEO👁"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ STILLAR BO‘LIMIDASIZ, BO‘LIMDAN O‘ZINGIZGA KERAKLI STILNI TANLANG👇",
        'reply_markup'=>$kstil,
    ]);
}

// KO'ZGA HARF VIDEO BO'LIMI BOSHLANISHI

if ($text == "👁BIRINCHI STIL👁"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZGA QAYSI BIRI KERAK👇!",
        'reply_markup'=>$kozga,
    ]);
}

if ($text == "🫶A"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/4",
        'caption'=>"A❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶B"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/5",
        'caption'=>"B❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶D"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/6",
        'caption'=>"D❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶E"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/7",
        'caption'=>"E❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶F"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/8",
        'caption'=>"F❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶G"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/9",
        'caption'=>"G❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶H"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/10",
        'caption'=>"H❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶I"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/11",
        'caption'=>"I❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶J"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/12",
        'caption'=>"J❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶K"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/13",
        'caption'=>"K❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶L"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/14",
        'caption'=>"L❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶M"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/15",
        'caption'=>"M❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶N"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/16",
        'caption'=>"N❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶O"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/17",
        'caption'=>"o❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶P"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/18",
        'caption'=>"P❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶Q"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/19",
        'caption'=>"Q❤ harfiga video tayyor 😉

➖➖➖➖➖n
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶R"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/20",
        'caption'=>"R❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶S"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/21",
        'caption'=>"S❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶T"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/22",
        'caption'=>"T❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶U"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/32",
        'caption'=>"U❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶V"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/24",
        'caption'=>"V❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶X"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/25",
        'caption'=>"X❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶Y"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/26",
        'caption'=>"Y❤Ю harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶Z"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/27",
        'caption'=>"Z❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶O'"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hozirda BOTIMIZ bu harfga video tayyorlay olmadi...!😐

🤫Lekin siz guruhimiz orqali adminlarga video zakaz qilishingiz mumkin👇🏻

https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶G'"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hozirda BOTIMIZ bu harfga video tayyorlay olmadi...!😐

🤫Lekin siz guruhimiz orqali adminlarga video zakaz qilishingiz mumkin👇🏻

https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶SH"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/30",
        'caption'=>"SH❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶CH"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hozirda BOTIMIZ bu harfga video tayyorlay olmadi...!😐

🤫Lekin siz guruhimiz orqali adminlarga video zakaz qilishingiz mumkin👇🏻

https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🫶Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ STILLAR BO‘LIMIGA QAYTDINGIZ, BO‘LIMDAN O‘ZINGIZGA KERAKLI STILNI TANLANG👇",
        'reply_markup'=>$kstil,
    ]);
}

// Ko‘zga stil 2

$kozga2 = json_encode([
    'resize_keyboard'=>true,
    'keyboard'=>[
    [['text'=>"❤️‍🩹A"],['text'=>"❤️‍🩹B"],['text'=>"❤️‍🩹D"],['text'=>"❤️‍🩹E"],['text'=>"❤️‍🩹F"]],[['text'=>"❤️‍🩹G"],['text'=>"❤️‍🩹H"],['text'=>"❤️‍🩹I"],['text'=>"❤️‍🩹J"],['text'=>"❤️‍🩹K"]],[['text'=>"❤️‍🩹L"],['text'=>"❤️‍🩹M"],['text'=>"❤️‍🩹N"],['text'=>"❤️‍🩹O"],['text'=>"❤️‍🩹P"]],[['text'=>"❤️‍🩹Q"],['text'=>"❤️‍🩹R"],['text'=>"❤️‍🩹S"],['text'=>"❤️‍🩹T"],['text'=>"❤️‍🩹U"]],[['text'=>"❤️‍🩹V"],['text'=>"❤️‍🩹X"],['text'=>"❤️‍🩹Y"],['text'=>"❤️‍🩹Z"],['text'=>"❤️‍🩹O'"]],[['text'=>"❤️‍🩹G'"],['text'=>"❤️‍🩹SH"],['text'=>"❤️‍🩹CH"]],[['text'=>"❤️‍🩹Orqaga"]],
    ]
    ]);
    
if ($text == "👁IKKINCHI STIL👁"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZGA QAYSI BIRI KERAK👇!",
        'reply_markup'=>$kozga2,
    ]);
}

if ($text == "❤️‍🩹A"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/125",
        'caption'=>"A❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹B"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/126",
        'caption'=>"B❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹D"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/127",
        'caption'=>"D❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹E"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/128",
        'caption'=>"E❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹F"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/129",
        'caption'=>"F❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹G"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/131",
        'caption'=>"G❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹H"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hozirda BOTIMIZ bu harfga video tayyorlay olmadi...!😐

🤫Lekin siz guruhimiz orqali adminlarga video zakaz qilishingiz mumkin👇🏻

https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1", 
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹I"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/132",
        'caption'=>"I❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹J"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/133",
        'caption'=>"J❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹K"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/134",
        'caption'=>"K❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹L"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/135",
        'caption'=>"L❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹M"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/136",
        'caption'=>"M❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹N"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/137",
        'caption'=>"N❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹O"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/138",
        'caption'=>"o❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹P"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hozirda BOTIMIZ bu harfga video tayyorlay olmadi...!😐

🤫Lekin siz guruhimiz orqali adminlarga video zakaz qilishingiz mumkin👇🏻

https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹Q"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hozirda BOTIMIZ bu harfga video tayyorlay olmadi...!😐

🤫Lekin siz guruhimiz orqali adminlarga video zakaz qilishingiz mumkin👇🏻

https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹R"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/139",
        'caption'=>"R❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹S"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/140",
        'caption'=>"S❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹T"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/141",
        'caption'=>"T❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹U"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hozirda BOTIMIZ bu harfga video tayyorlay olmadi...!😐

🤫Lekin siz guruhimiz orqali adminlarga video zakaz qilishingiz mumkin👇🏻

https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹V"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hozirda BOTIMIZ bu harfga video tayyorlay olmadi...!😐

🤫Lekin siz guruhimiz orqali adminlarga video zakaz qilishingiz mumkin👇🏻

https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹X"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/142",
        'caption'=>"X❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹Y"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/143",
        'caption'=>"Y❤Ю harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹Z"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/144",
        'caption'=>"Z❤ harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!
📹Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹O'"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hozirda BOTIMIZ bu harfga video tayyorlay olmadi...!😐

🤫Lekin siz guruhimiz orqali adminlarga video zakaz qilishingiz mumkin👇🏻

https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹G'"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hozirda BOTIMIZ bu harfga video tayyorlay olmadi...!😐

🤫Lekin siz guruhimiz orqali adminlarga video zakaz qilishingiz mumkin👇🏻

https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹SH"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hozirda BOTIMIZ bu harfga video tayyorlay olmadi...!😐

🤫Lekin siz guruhimiz orqali adminlarga video zakaz qilishingiz mumkin👇🏻

https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹CH"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hozirda BOTIMIZ bu harfga video tayyorlay olmadi...!😐

🤫Lekin siz guruhimiz orqali adminlarga video zakaz qilishingiz mumkin👇🏻

https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "❤️‍🩹Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ STILLAR BO‘LIMIGA QAYTDINGIZ, BO‘LIMDAN O‘ZINGIZGA KERAKLI STILNI TANLANG👇",
        'reply_markup'=>$kstil,
    ]);
}


// KEYINGI BO‘LIM

$stillar = json_encode([
    'resize_keyboard'=>true,
    'keyboard'=>[
    [['text'=>"❣️BIRINCHI STIL🎁"],['text'=>"❣️IKKINCHI STIL🎁"]],[['text'=>"❣️UCHINCHI STIL🎁"],['text'=>"❣️TO‘RTINCHI STIL🎁"]],[['text'=>"🔄Orqaga"]],
    ]
    ]);
    
if ($text == "🔄Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ ASOSIY MENYUGA QAYTDINGIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇",
        'reply_markup'=>$asosiy,
    ]);
}

// BIRINCHI STIL BO‘LMI
    
if ($text == "🥰HARFLARGA VIDEOLAR😎"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ STILLAR BO‘LIMIDASIZ, BO‘LIMDAN O‘ZINGIZGA KERAKLI STILNI TANLANG👇",
        'reply_markup'=>$stillar,
    ]);
}

$harfga = json_encode([
    'resize_keyboard'=>true,
    'keyboard'=>[
    [['text'=>"💜A"],['text'=>"💜B"],['text'=>"💜D"],['text'=>"💜E"],['text'=>"💜F"]],[['text'=>"💜G"],['text'=>"💜H"],['text'=>"💜I"],['text'=>"💜J"],['text'=>"💜K"]],[['text'=>"💜L"],['text'=>"💜M"],['text'=>"💜N"],['text'=>"💜O"],['text'=>"💜P"]],[['text'=>"💜Q"],['text'=>"💜R"],['text'=>"💜S"],['text'=>"💜T"],['text'=>"💜U"]],[['text'=>"💜V"],['text'=>"💜X"],['text'=>"💜Y"],['text'=>"💜Z"],['text'=>"💜O'"]],[['text'=>"💜G'"],['text'=>"💜SH"],['text'=>"💜CH"]],[['text'=>"💜Orqaga"]],
    ]
    ]);
    
if ($text == "❣️BIRINCHI STIL🎁"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZGA QAYSI BIRI KERAK👇!",
        'reply_markup'=>$harfga,
    ]);
}

if ($text == "💜A"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/69",
        'caption'=>"A💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜B"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/70",
        'caption'=>"B💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜D"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/71",
        'caption'=>"D💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜E"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/72",
        'caption'=>"E💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜F"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/73",
        'caption'=>"F💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜G"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/74",
        'caption'=>"G💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜H"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/75",
        'caption'=>"H💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "??I"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/76",
        'caption'=>"I💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜J"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/77",
        'caption'=>"J💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜K"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/78",
        'caption'=>"K💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜L"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/79",
        'caption'=>"L💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜M"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/80",
        'caption'=>"M💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜N"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/81",
        'caption'=>"N💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜O"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/82",
        'caption'=>"O💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜P"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/83",
        'caption'=>"P💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜Q"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/84",
        'caption'=>"Q💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜R"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/85",
        'caption'=>"R💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜S"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/86",
        'caption'=>"S💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜T"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/87",
        'caption'=>"T💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜U"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/88",
        'caption'=>"U💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜V"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/89",
        'caption'=>"V💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜X"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/90",
        'caption'=>"X💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜Y"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/91",
        'caption'=>"Y💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜Z"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/93",
        'caption'=>"Z💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜O'"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/92",
        'caption'=>"O‘💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜G'"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/96",
        'caption'=>"G‘💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜SH"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/94",
        'caption'=>"SH💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜CH"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/95",
        'caption'=>"CH💜 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💜Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ STILLAR BO‘LIMIGA QAYTDINGIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇",
        'reply_markup'=>$stillar,
    ]);
}

// IKKINCHI STIL BO‘LMI

$harfga2 = json_encode([
    'resize_keyboard'=>true,
    'keyboard'=>[
    [['text'=>"💚A"],['text'=>"💚B"],['text'=>"💚D"],['text'=>"💚E"],['text'=>"💚F"]],[['text'=>"💚G"],['text'=>"💚H"],['text'=>"💚I"],['text'=>"💚J"],['text'=>"💚K"]],[['text'=>"💚L"],['text'=>"💚M"],['text'=>"💚N"],['text'=>"💚O"],['text'=>"💚P"]],[['text'=>"💚Q"],['text'=>"💚R"],['text'=>"💚S"],['text'=>"💚T"],['text'=>"💚U"]],[['text'=>"💚V"],['text'=>"💚X"],['text'=>"💚Y"],['text'=>"💚Z"],['text'=>"💚O'"]],[['text'=>"💚G'"],['text'=>"💚SH"],['text'=>"💚CH"]],[['text'=>"💚Orqaga"]],
    ]
    ]);
    
if ($text == "❣️IKKINCHI STIL🎁"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZGA QAYSI BIRI KERAK👇!",
        'reply_markup'=>$harfga2,
    ]);
}

if ($text == "💚A"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/97",
        'caption'=>"A💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚B"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/98",
        'caption'=>"B💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚D"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/99",
        'caption'=>"D💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚E"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/100",
        'caption'=>"E💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚F"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/101",
        'caption'=>"F💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚G"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/102",
        'caption'=>"G💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚H"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/103",
        'caption'=>"H💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚I"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/104",
        'caption'=>"I💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚J"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/105",
        'caption'=>"J💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚K"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/106",
        'caption'=>"K💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚L"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/107",
        'caption'=>"L💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚M"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/108",
        'caption'=>"M💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚N"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/109",
        'caption'=>"N💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚O"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/110",
        'caption'=>"O💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚P"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/111",
        'caption'=>"P💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚Q"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/112",
        'caption'=>"Q💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚R"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/113",
        'caption'=>"R💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚S"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/114",
        'caption'=>"S💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚T"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/115",
        'caption'=>"T💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚U"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/116",
        'caption'=>"U💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚V"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/117",
        'caption'=>"V💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚X"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/118",
        'caption'=>"X💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚Y"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/119",
        'caption'=>"Y💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚Z"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/120",
        'caption'=>"Z💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚O‘"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/121",
        'caption'=>"O‘💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚G‘"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/122",
        'caption'=>"G‘💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚SH"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/123",
        'caption'=>"SH💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚CH"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/124",
        'caption'=>"CH💚 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💚Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ STILLAR BO‘LIMIGA QAYTDINGIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇",
        'reply_markup'=>$stillar,
    ]);
}

// UCHINCHI BO‘LIM

$harfga3 = json_encode([
    'resize_keyboard'=>true,
    'keyboard'=>[
    [['text'=>"🧡A"],['text'=>"🧡B"],['text'=>"🧡D"],['text'=>"🧡E"],['text'=>"🧡F"]],[['text'=>"🧡G"],['text'=>"🧡H"],['text'=>"🧡I"],['text'=>"🧡J"],['text'=>"🧡K"]],[['text'=>"🧡L"],['text'=>"🧡M"],['text'=>"🧡N"],['text'=>"🧡O"],['text'=>"🧡P"]],[['text'=>"🧡Q"],['text'=>"🧡R"],['text'=>"🧡S"],['text'=>"🧡T"],['text'=>"🧡U"]],[['text'=>"🧡V"],['text'=>"🧡X"],['text'=>"🧡Y"],['text'=>"🧡Z"],['text'=>"🧡O'"]],[['text'=>"🧡G'"],['text'=>"🧡SH"],['text'=>"🧡CH"]],[['text'=>"🧡Orqaga"]],
    ]
    ]);
    
if ($text == "❣️UCHINCHI STIL🎁"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZGA QAYSI BIRI KERAK👇!",
        'reply_markup'=>$harfga3,
    ]);
}

if ($text == "🧡A"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/169",
        'caption'=>"A🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡B"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/170",
        'caption'=>"B🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡D"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/171",
        'caption'=>"D🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡E"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/172",
        'caption'=>"E🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡F"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/173",
        'caption'=>"F🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡G"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/174",
        'caption'=>"G🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡H"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/175",
        'caption'=>"H🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡I"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/176",
        'caption'=>"I🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡J"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/177",
        'caption'=>"J🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡K"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/178",
        'caption'=>"K🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡L"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/179",
        'caption'=>"L🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡M"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/180",
        'caption'=>"M🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡N"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/181",
        'caption'=>"N🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡O"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/182",
        'caption'=>"O🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡P"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/183",
        'caption'=>"P🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡Q"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/184",
        'caption'=>"Q🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡R"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/185",
        'caption'=>"R🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡S"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/186",
        'caption'=>"S🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡T"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/187",
        'caption'=>"T🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡U"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/188",
        'caption'=>"U🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡V"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/189",
        'caption'=>"V🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡X"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/190",
        'caption'=>"X🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡Y"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/191",
        'caption'=>"Y🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡Z"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/192",
        'caption'=>"Z🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡O'"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/193",
        'caption'=>"O‘🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡G'"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/194",
        'caption'=>"G‘🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡SH"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/195",
        'caption'=>"SH🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡CH"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/196",
        'caption'=>"CH🧡 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "🧡Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ STILLAR BO‘LIMIGA QAYTDINGIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇",
        'reply_markup'=>$stillar,
    ]);
}

// TO‘RTINCHI BO‘LIM

$harfga = json_encode([
    'resize_keyboard'=>true,
    'keyboard'=>[
    [['text'=>"💛A"],['text'=>"💛B"],['text'=>"💛D"],['text'=>"💛E"],['text'=>"💛F"]],[['text'=>"💛G"],['text'=>"💛H"],['text'=>"💛I"],['text'=>"💛J"],['text'=>"💛K"]],[['text'=>"💛L"],['text'=>"💛M"],['text'=>"💛N"],['text'=>"💛O"],['text'=>"💛P"]],[['text'=>"💛Q"],['text'=>"💛R"],['text'=>"💛S"],['text'=>"💛T"],['text'=>"💛U"]],[['text'=>"💛V"],['text'=>"💛X"],['text'=>"💛Y"],['text'=>"💛Z"],['text'=>"💛O'"]],[['text'=>"💛G'"],['text'=>"💛SH"],['text'=>"💛CH"]],[['text'=>"💛Orqaga"]],
    ]
    ]);
    
if ($text == "❣️TO‘RTINCHI STIL🎁"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZGA QAYSI BIRI KERAK👇!",
        'reply_markup'=>$harfga,
    ]);
}

if ($text == "💛A"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/221",
        'caption'=>"A💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛B"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/222",
        'caption'=>"B💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛D"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/223",
        'caption'=>"D💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛E"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/224",
        'caption'=>"E💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛F"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/225",
        'caption'=>"F💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛G"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/226",
        'caption'=>"G💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛H"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/227",
        'caption'=>"H💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛I"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/228",
        'caption'=>"I💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛J"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/229",
        'caption'=>"J💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛K"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/230",
        'caption'=>"K💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛L"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/231",
        'caption'=>"L💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛M"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/232",
        'caption'=>"M💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛N"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/233",
        'caption'=>"N💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛O"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/234",
        'caption'=>"O💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛P"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/235",
        'caption'=>"P💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛Q"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/236",
        'caption'=>"Q💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛R"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/248",
        'caption'=>"R💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛S"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/237",
        'caption'=>"S💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛T"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/238",
        'caption'=>"T💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛U"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/239",
        'caption'=>"U💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛V"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/240",
        'caption'=>"V💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛X"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/241",
        'caption'=>"X💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛Y"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/242",
        'caption'=>"Y💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛Z"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/243",
        'caption'=>"Z💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛O'"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/244",
        'caption'=>"O‘💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛G'"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/245",
        'caption'=>"G‘💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛SH"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/246",
        'caption'=>"SH💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛CH"){
    bot('SendVideo',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'video'=>"https://t.me/ismlargavideolar_database/247",
        'caption'=>"CH💛 harfiga video tayyor 😉

➖➖➖➖➖
🤖 @ismlargavideolar_uzbot  tomonidan yasab berildi!

✅Boshqa harfga yozish uchun menyudan shunchaki istalgan harfingizni tanlang!",
        'reply_markup'=>$ulashish,
    ]);
}

if ($text == "💛Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ STILLAR BO‘LIMIGA QAYTDINGIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇",
        'reply_markup'=>$stillar,
    ]);
}
    
 if ($text == "😍ISMLARGA VIDEOLAR🤗"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n 
🤫 siz guruhimiz orqali adminlarga video zakaz qilishingiz mumkin👇🏻

https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1
https://t.me/OKEAN_STUDION1",
        'reply_markup'=>$asosiy,
    ]);
}

 if ($text == "💕Paralik rasmlar💞"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n 
🤫 siz kanalimiz orqali 100 dan ortiq paralik rasmlarni topishingiz mumkin👇🏻

https://t.me/paralikrasmlarN1
https://t.me/paralikrasmlarN1
https://t.me/paralikrasmlarN1",
        'reply_markup'=>$rasm,
    ]);
}

// FOYDALI BO‘LIMI
$foydali = json_encode([
                'resize_keyboard'=>true,
                'keyboard'=>[
[['text'=>"🎲O‘yinlar"],['text'=>"💾QR-Kod"]],[['text'=>"🇺🇿Telegram tilllari"],['text'=>"❇️Telegram mavzulari"]],[['text'=>"💰Valyutalar kurslari"],['text'=>"🌤Ob-havo ma'lumotlari"]],[['text'=>"🇺🇿Orqaga"]],
    ]
    ]);

if ($text == "🌐FOYDALI BO‘LIM🌐"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ FOYDALI BO‘LIMIDASIZ, MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇",
        'reply_markup'=>$foydali,
    ]);
}

if ($text == "🇺🇿Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ ASOSIY MENYUGA QAYTDINGIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇",
        'reply_markup'=>$asosiy,
    ]);
}

$til = json_encode([
                'inline_keyboard'=>[
[['text'=>"🇺🇿O‘zbek tili | telefon uchun",'url'=>"tg://setlanguage?lang=uz-beta"]],[['text'=>"🇺🇿Ўзбек тили | telefon uchun",'url'=>"tg://setlanguage?lang=uzbekcyr"]],[['text'=>"🇷🇺Русский язык | telefon uchun",'url'=>"tg://setlanguage?lang=ru"]],[['text'=>"🇺🇸English language | telefon uchun",'url'=>"tg://setlanguage?lang=en"]],[['text'=>"🇺🇿O‘zbek tili | WINDOWS uchun",'url'=>"tg://setlanguage?lang=uz-beta"]],[['text'=>"🇷🇺Русский язык | WINDOWS uchun",'url'=>"tg://setlanguage?lang=ru"]],[['text'=>"🇺🇿Ўзбек тили | telefon uchun",'url'=>"tg://setlanguage?lang=uzbekcyr"]],[['text'=>"🇺🇸English language | telefon uchun",'url'=>"tg://setlanguage?lang=en"]],
    ] 
    ]);

if ($text == "🇺🇿Telegram tilllari"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n ⚜️Telegramingiz tilini osongina o'zgartirish
     uchun quyidagi tillardan birini tanlang👇",
        'reply_markup'=>$til, 
        ]); 
}

$mavzu = json_encode([
                'inline_keyboard'=>[
[['text'=>"Abstract",'url'=>"https://t.me/addtheme/abstractphx"]],[['text'=>"Milano Theme",'url'=>"https://t.me/addtheme/telegathemes_81"]],[['text'=>"VK",'url'=>"https://t.me/addtheme/Dsvf7DEsjsQEKzhb"]],[['text'=>"Love protection",'url'=>"https://t.me/addtheme/telegathemes_5"]],[['text'=>"Iphone uchun 1",'url'=>"https://t.me/addtheme/IOSTelegramThemes2023_24April"]],[['text'=>"Iphone uchun 2",'url'=>"https://t.me/addtheme/IOSTelegramThemes2023_20May"]],[['text'=>"Iphone uchun 3",'url'=>"https://t.me/addtheme/IOSTelegramThemes2023_4April"]],[['text'=>"Iphone uchun 4 Love mavzu",'url'=>"https://t.me/addtheme/IOSTelegramThemes2022_11June"]], 
    ] 
    ]);

if ($text == "❇️Telegram mavzulari"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n ⚜️Telegramingiz mavzusini osongina o'zgartirish
     uchun quyidagi mavzulardan birini tanlang👇",
        'reply_markup'=>$mavzu, 
        ]); 
}

// OB HAVO

$vil = json_encode([
'inline_keyboard'=>[
[['text'=>"🌁Samarqand",'callback_data'=>"ob=samarqand"],['text'=>"🌁Farg'ona",'callback_data'=>"ob=fergana"]],
[['text'=>"🌁Xorazm",'callback_data'=>"ob=xorazm"],['text'=>"🌁Xiva",'callback_data'=>"ob=xiva"]],
[['text'=>"🌁Toshkent",'callback_data'=>"ob=toshkent"],['text'=>"🌁Buxoro",'callback_data'=>"ob=buxoro"]],
[['text'=>"🌁Navoi",'callback_data'=>"ob=navoi"],['text'=>"🌁Andijon",'callback_data'=>"ob=andijon"]],
[['text'=>"🌁Sirdaryo",'callback_data'=>"ob=sirdaryo"],['text'=>"🌁Namangan",'callback_data'=>"ob=namangan"]],
[['text'=>"🌁Qashqadaryo",'callback_data'=>"ob=qashqadaryo"],['text'=>"🌁Surxandaryo",'callback_data'=>"ob=surxandaryo"]],
[['text'=>"◀️ Orqaga",'callback_data'=>"asosiyga"]],
]
]);

if($data == "asosiyga"){
	bot('deleteMessage',[
	'chat_id'=>$cid2,
	'message_id'=>$mid2,
	]);
bot('sendMessage',[
'chat_id'=>$cid2,
'text'=>"Orqaga qaytdingiz",
'reply_markup'=>$vil, 
]);
}

if(mb_stripos($data,"ob") !== false){
       $ex = explode("=",$data);
    $s = $ex[1];
$a=json_decode(file_get_contents("https://api.openweathermap.org/data/2.5/weather?q=$s&units=metric&appid=da8e2c9adc2bf342f0d697f6cb7e5568"),true);
$t=$a["main"]["temp"];
$n=$a["main"]["humidity"];
$tez=$a["wind"]["speed"];
$sh=$a["wind"]["gust"];
$dav=$a["sys"]["country"];
$ti=$a["timezone"];
$bu=$a["clouds"]["all"];
$qch=$a["sys"]["sunrise"];
$qb=$a["sys"]["sunset"];
bot('editMessageText',[
'chat_id'=>$cid2,
'message_id'=>$mid2,
'text'=>"<b>☀️ Harorat: $t °\n💦 Namlik: $n %\n💨 Tezlik: $tez km/h\n🌬 Shamol tezlik: $sh km/h\n☀️ Quyosh chiqishi: $qch\n🌥 Quyosh botishi: $qb\n⏱ Vaqt mintaqasi: $ti\n☁️ Bulutlar: $bu ta\n\n🛣 Mamlakat kodi: $dav</b>",
'parse_mode'=>"html",
'reply_markup'=>json_encode([
'inline_keyboard'=>[
[['text'=>"◀️ Orqaga",'callback_data'=>"asosiyga"]],
]
])
]);
}

if ($text == "🌤Ob-havo ma'lumotlari"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n Viloyatingizni tanlang👇",
        'reply_markup'=>$vil, 
        ]); 
}

// Valyuta kursi

function kurs(){
       $response = "";
       $xml = file_get_contents("http://cbu.uz/uzc/arkhiv-kursov-valyut/xml/");
       $m = new SimpleXMLElement($xml);
       foreach ($m as $val) {
           if($val->Ccy == 'USD'){
               $response .= "1 Aqsh dollori - " . $val->Rate . " sum\n\n";
           }
           if($val->Ccy == 'AED'){
               $response .= "1 BAA dirhami - " . $val->Rate . " sum\n";
           }
           if($val->Ccy == 'AFN'){
               $response .= "1 Afgoniston Afgoni - " . $val->Rate . " sum\n";
           }
           if($val->Ccy == 'AMD'){
               $response .= "1 Armaniston drami - " . $val->Rate . " sum\n";
           }
           if($val->Ccy == 'ARS'){
               $response .= "1 Argentika pesosi - " . $val->Rate . " sum\n";
           }
           if($val->Ccy == 'AUD'){
               $response .= "1 Avstraliya dollori - " . $val->Rate . " sum\n";
           }
           if($val->Ccy == 'AZN'){
               $response .= "1 Ozarbayjon manati - " . $val->Rate . " sum\n";
           }
           if($val->Ccy == 'BDT'){
               $response .= "1 Bangladesh Takasi - " . $val->Rate . " sum\n";
           }
           if($val->Ccy == 'BGN'){
               $response .= "1 Bolgariya levi - " . $val->Rate . " so‘m/uz\n";
           }
           if($val->Ccy == 'BDH'){
               $response .= "1 Bahrayn dinori - " . $val->Rate . " so‘m/uz\n";
           }
           if($val->Ccy == 'BND'){
               $response .= "1 Bruney dollori - " . $val->Rate . " so‘m/uz\n";
           }
           if($val->Ccy == 'BRL'){
               $response .= "1 Braziliya reali - " . $val->Rate . " so‘m/uz\n";
           }
           if($val->Ccy == 'BYN'){
               $response .= "1 Belorus rubli - " . $val->Rate . " so‘m/uz\n";
           }
           if($val->Ccy == 'ZAR'){
               $response .= "🔄So'nggi Yangilanishlar: " . $val->date."\n";
           }
           if($val->Ccy == 'JPY'){
               $response .= "1 yaponiya - " . $val->Rate . " so‘m/uz\n";
           }  if($val->Ccy == 'RUB'){
               $response .= "1 Rossiya rubli - " . $val->Rate . " so‘m/uz\n";
           }
       }
      return $response;
   }

if($text == "💰Valyutalar kurslari"){
  bot('sendMessage',[
  'chat_id'=>$chat_id,
  'text'=>kurs(), 
'parse_mode'=>'html',   
]);
}

// ismlarga rasmlar

$ismlar2 = json_encode([
                   'resize_keyboard'=>true,
                   'keyboard'=>[
[['text'=>"👱‍♂️Yigitlar uchun"],['text'=>"👩‍🦰Qizlar uchun"]],[['text'=>" ❇️Orqaga"]], 
] 
]); 

$yigitlars = json_encode([
'resize_keyboard'=>true, 
'keyboard'=>[
[['text'=>"🙋🏻‍♂️1"],['text'=>"🙋🏻‍♂️2"],['text'=>"🙋🏻‍♂️3"]],[['text'=> "🚫Bekor qilish"]], 
] 
]); 

if ($text == "👱‍♂️Yigitlar uchun"){
    bot('SendPhoto',[
        'chat_id'=>$chat_id, 
        'parse_mode'=>"html",
        'photo'=>"https://t.me/ismlargavideolar_database/249", 
        'caption'=>"$name , O‘zingizga yoqqan👆🏻 stilni tanlang👇🏻", 
         'reply_markup'=>$yigitlars, 
        ]); 
}

if ($text == "❤️‍🔥Ismlarga rasmlar"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n Kerakli menyuni tanlang👇",
        'reply_markup'=>$ismlar2, 
        ]); 
}

if ($text == "🚫Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n FOYDALI BO‘LIMIGA QAYTDINGIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇",
        'reply_markup'=>$rasm,
    ]);
}

$ochir = json_encode([
'inline_keyboard'=>[
[['text'=>"🗑O‘chirish",'callback_data'=>"ochirish"]],[['text'=>"👥Do‘stlarga ulashish↪️",'url'=>"https://t.me/share/url?text=%20Bu%20botga%20sizni%20ham%20taklif%20etaman!%20O'zingiz%20uchun%20ajoyib%20videolar%20yasab%20oling✅%0A%0A👉%20@ismlargavideolar_uzbot%20🎁"]],
]
]); 

if($data == "ochirish"){
	bot('deleteMessage',[
	'chat_id'=>$cid2,
	'message_id'=>$mid2,
	]);
	} 

if($text== "🙋🏻‍♂️1"){
bot('SendMessage',[
'chat_id'=>$chat_id,
'message_id'=>$message_id,
'text'=>"<b>Ismingizni kiriting:</b>",
'parse_mode'=>"html",
]);
file_put_contents("step/$chat_id.step","erkak1");
} 
if($step2=="erkak1"){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"☇ Tayorlanmoqda kuting ...", 
]); 
file_put_contents("ism/$chat_id.ism","$text"); 
file_put_contents("step/$chat_id.step","");
bot('sendphoto',[
'chat_id'=>$chat_id,
'photo'=>"http://u8481.xvest6.ru/Apilar/Fildirbot/Yigitlar/1/2.php?text=$text",
'caption'=>"<b>$text ismiga, 🤖 $botuser rasm tayyorlab berdi ✨!
\n\n  $reklama </b>",
 'parse_mode'=>"html", 
 'reply_markup'=>$ochir, 
 ]);
unlink("ism/$chat_id.ism");
unlink("step/$chat_id.step");
}

if($text== "🙋🏻‍♂️2"){
bot('SendMessage',[
'chat_id'=>$chat_id,
'message_id'=>$message_id,
'text'=>"<b>Ismingizni kiriting:</b>",
'parse_mode'=>"html",
]);
file_put_contents("step/$chat_id.step","erkak2");
} 
if($step2=="erkak2"){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"☇ Tayorlanmoqda kuting ...", 
]); 
file_put_contents("ism/$chat_id.ism","$text"); 
file_put_contents("step/$chat_id.step","");
bot('sendphoto',[
'chat_id'=>$chat_id,
'photo'=>"http://u8481.xvest6.ru/Apilar/Fildirbot/Yigitlar/2/2.php?text=$text",
'caption'=>"<b>$text ismiga, 🤖 $botuser rasm tayyorlab berdi ✨!
\n\n  $reklama </b>",
 'parse_mode'=>"html", 
 'reply_markup'=>$ochir, 
 ]);
unlink("ism/$chat_id.ism");
unlink("step/$chat_id.step");
}

if($text== "🙋🏻‍♂️3"){
bot('SendMessage',[
'chat_id'=>$chat_id,
'message_id'=>$message_id,
'text'=>"<b>Ismingizni kiriting:</b>",
'parse_mode'=>"html",
]);
file_put_contents("step/$chat_id.step","erkak3");
} 
if($step2=="erkak3"){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"☇ Tayorlanmoqda kuting ...", 
]); 
file_put_contents("ism/$chat_id.ism","$text"); 
file_put_contents("step/$chat_id.step","");
bot('sendphoto',[
'chat_id'=>$chat_id,
'photo'=>"http://u8481.xvest6.ru/Apilar/Fildirbot/Yigitlar/3/2.php?text=$text",
'caption'=>"<b>$text ismiga, 🤖 $botuser rasm tayyorlab berdi ✨!
\n\n  $reklama </b>",
 'parse_mode'=>"html", 
 'reply_markup'=>$ochir, 
 ]);
unlink("ism/$chat_id.ism");
unlink("step/$chat_id.step");
}

$qizlars= json_encode([
'resize_keyboard'=>true, 
'keyboard'=>[
[['text'=>"🙋🏻‍♀️1"],['text'=>"🙋🏻‍♀️2"],['text'=>"🙋🏻‍♀️3"]],[['text'=> "🚫Bekor qilish"]], 
] 
]); 

if ($text == "👩‍🦰Qizlar uchun"){
    bot('SendPhoto',[
        'chat_id'=>$chat_id, 
        'parse_mode'=>"html",
        'photo'=>"https://t.me/ismlargavideolar_database/250", 
        'caption'=>"$name , O‘zingizga yoqqan👆🏻 stilni tanlang👇🏻", 
         'reply_markup'=>$qizlars, 
        ]); 
}

if($text=="🙋🏻‍♀️1"){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"<b>Ismingizni kiriting:</b>",
'parse_mode'=>"html",
'reply_markup'=>$bekor_qilish, 
]);
file_put_contents("step/$chat_id.step","ayol1");
}
if($step2=="ayol1"){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"☇ Tayorlanmoqda kuting ...",
]); 
file_put_contents("ism/$chat_id.ism","$text"); 
file_put_contents("step/$chat_id.step","");
bot('sendphoto',[
'chat_id'=>$chat_id,
'photo'=>"http://u8481.xvest6.ru/Apilar/Fildirbot/Qizlarga/1/2.php?text=$text",
'caption'=>"<b>$text ismiga, 🤖 $botuser rasm tayyorlab berdi ✨!
\n\n  $reklama  </b>",
 'parse_mode'=>"html",
 'reply_markup'=>$ochir, 
]);
unlink("ism/$chat_id.ism");
unlink("step/$chat_id.step");
}

if($text=="🙋🏻‍♀️2"){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"<b>Ismingizni kiriting:</b>",
'parse_mode'=>"html",
'reply_markup'=>$bekor_qilish, 
]);
file_put_contents("step/$chat_id.step","ayol2");
}
if($step2=="ayol2"){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"☇ Tayorlanmoqda kuting ...",
]); 
file_put_contents("ism/$chat_id.ism","$text"); 
file_put_contents("step/$chat_id.step","");
bot('sendphoto',[
'chat_id'=>$chat_id,
'photo'=>"http://u8481.xvest6.ru/Apilar/Fildirbot/Qizlarga/2/2.php?text=$text",
'caption'=>"<b>$text ismiga, 🤖 $botuser rasm tayyorlab berdi ✨!
\n\n  $reklama  </b>",
 'parse_mode'=>"html",
 'reply_markup'=>$ochir, 
]);
unlink("ism/$chat_id.ism");
unlink("step/$chat_id.step");
}

if($text=="🙋🏻‍♀️3"){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"<b>Ismingizni kiriting:</b>",
'parse_mode'=>"html",
'reply_markup'=>$bekor_qilish, 
]);
file_put_contents("step/$chat_id.step","ayol3");
}
if($step2=="ayol3"){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"☇ Tayorlanmoqda kuting ...",
]); 
file_put_contents("ism/$chat_id.ism","$text"); 
file_put_contents("step/$chat_id.step","");
bot('sendphoto',[
'chat_id'=>$chat_id,
'photo'=>"http://u8481.xvest6.ru/Apilar/Fildirbot/Qizlarga/3/2.php?text=$text",
'caption'=>"<b>$text ismiga, 🤖 $botuser rasm tayyorlab berdi ✨!
\n\n  $reklama  </b>",
 'parse_mode'=>"html",
 'reply_markup'=>$ochir, 
]);
unlink("ism/$chat_id.ism");
unlink("step/$chat_id.step");
}

if ($text == "🚫Bekor qilish"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ ORQAGA QAYTDINGIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇",
        'reply_markup'=>$ismlar2,
    ]);
}

if ($text == "❇️Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n RASM BO‘LIMIGA QAYTDINGIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇",
        'reply_markup'=>$rasm,
    ]);
}

// Tug‘ilgan kun
$tk = json_encode([
                   'resize_keyboard'=>true,
                   'keyboard'=>[
[['text'=>"😎Yigitlar uchun"],['text'=>"🥰Qizlar uchun"]],[['text'=>"🎉Orqaga"]], 
] 
]); 

if ($text == "🎉Tug‘ulgan kun tabrik"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n Kerakli menyuni tanlang👇",
        'reply_markup'=>$tk, 
        ]); 
}

$tabriky = json_encode([
                'inline_keyboard'=>[
[['text'=>"🎉Tug‘ilgan kun egasiga yuborish↪️",'url'=>"https://t.me/share/url?text=%20http://u12364.xvest1.ru/ismlargavideolar/tugulgan_kun/index2.php?text=$text"]],[['text'=>"🗑O‘chirish",'callback_data'=>"ochirish"]],
    ]
    ]);

if($text=="😎Yigitlar uchun"){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"<b>Ismingizni kiriting:</b>",
'parse_mode'=>"html",
]);
file_put_contents("step/$chat_id.step","tabrik1");
}
if($step2=="tabrik1" ){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"☇ Tayyorlanmoqda kuting ...",
]); 
file_put_contents("ism/$chat_id.ism","$text"); 
file_put_contents("step/$chat_id.step","");
bot('sendphoto',[
'chat_id'=>$chat_id,
'photo'=>"http://u12364.xvest1.ru/ismlargavideolar/tugulgan_kun/index2.php?text=$text",
'caption'=>"<b>$text Tug‘ilgan kuningiz bo‘lsin muborak! \n\n🤖 $botuser rasm tayyorlab berdi ✨!
\n\n  $reklama  </b>",
 'parse_mode'=>"html",
 'reply_markup'=>$tabriky, 
]);
unlink("ism/$chat_id.ism");
unlink("step/$chat_id.step");
}

$tabrikq = json_encode([
                'inline_keyboard'=>[
[['text'=>"🎉Tug‘ilgan kun egasiga yuborish↪️",'url'=>"https://t.me/share/url?text=%20https://yaxyobek.uzxost.ru/Ismlargavideolar/Ismlargavideolar/tugulgan_kun/index.php?text=$text"]],[['text'=>"🗑O‘chirish",'callback_data'=>"ochirish"]],
    ]
    ]);

if($text=="🥰Qizlar uchun"){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"<b>Ismingizni kiriting:</b>",
'parse_mode'=>"html",
]);
file_put_contents("step/$chat_id.step","tabrik2");
}
if($step2=="tabrik2" ){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"☇ Tayorlanmoqda kuting ...",
]); 
file_put_contents("ism/$chat_id.ism","$text"); 
file_put_contents("step/$chat_id.step","");
bot('sendphoto',[
'chat_id'=>$chat_id,
'photo'=>"https://yaxyobek.uzxost.ru/Ismlargavideolar/Ismlargavideolar/tugulgan_kun/index.php?text=$text",
'caption'=>"<b>$text Tug‘ilgan kuningiz bo‘lsin muborak! \n\n🤖 $botuser rasm tayyorlab berdi ✨!
\n\n  $reklama  </b>",
 'parse_mode'=>"html",
 'reply_markup'=>$tabrikq, 
]);
unlink("ism/$chat_id.ism");
unlink("step/$chat_id.step");
}

if ($text == "🎉Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n RASM BO‘LIMIGA QAYTDINGIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇",
        'reply_markup'=>$rasm, 
    ]);
}


if($text=="🟡Humans stilida ism🟡"){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"<b>Ismingizni kiriting:</b>",
'parse_mode'=>"html",
]);
file_put_contents("step/$chat_id.step","humans1");
}
if($step2=="humans1" ){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"☇ Tayorlanmoqda kuting ...",
]); 
file_put_contents("ism/$chat_id.ism","$text"); 
file_put_contents("step/$chat_id.step","");

bot('sendphoto',[
'chat_id'=>$chat_id,
'photo'=>"https://yaxyobek.uzxost.ru/Ismlargavideolar/Ismlargavideolar/Humans/humans.php?text=$text",
'caption'=>"<b>$text ismiga Humans stilidagi rasm\n\n🤖 $botuser tayyorlab berdi ✨!
\n\n  $reklama  </b>",
 'parse_mode'=>"html",
 'reply_markup'=>$ochir, 
]);
unlink("ism/$chat_id.ism");
unlink("step/$chat_id.step");
}

// O‘YINLAR

$oyinlar = json_encode([
                'resize_keyboard'=>true,
                'keyboard'=>[
[['text'=>"🤵🏻Mafiya o‘yini"],['text'=>"♟️Shaxmat"]],[['text'=>"🎲Narda"]],[['text'=>"📲Orqaga"]],
    ]
    ]);
    
if ($text == "📲Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n FOYDALI BO‘LIMIGA QAYTDINGIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇",
        'reply_markup'=>$foydali,
    ]);
}

if($text== "🎲Narda"){
    $url =  bot('sendDice',[ 
    'emoji'=>"🎲",
    'chat_id'=>$chat_id,
])->result->dice->value;
    bot('SendMessage',[
    'chat_id'=>$chat_id,
    'text'=>"✅Natijangiz : $url",
]);
}

if ($text == "♟️Shaxmat"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ SHAXMAT O‘YININI PASTDAGI BOTGA KIRIB O‘YNASHINGIZ MUMKIN👇\n\n  @GameFactoryBot",
        'reply_markup'=>$oyinlar,
    ]);
}

if ($text == "🤵🏻Mafiya o‘yini"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ MAFIYA O‘YININI PASTDAGI GURUHGA KIRIB O‘YNASHINGIZ MUMKIN👇\n\n  https://t.me/Mafiya_UZB_No1",
        'reply_markup'=>$oyinlar,
    ]);
}

if ($text == "🎲O‘yinlar"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n HOHLAGAN O‘YINGIZNI TANLANG👇",
        'reply_markup'=>$oyinlar,
    ]);
}

// QR KOD 
$qrkod = json_encode([
                'resize_keyboard'=>true,
                'keyboard'=>[
[['text'=>"💾QR-Kodni o‘qish"],['text'=>"💾QR-Kod yasash"]],[['text'=>"↪️Orqaga"]],
    ]
    ]);
    
if ($text == "↪️Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n FOYDALI BO‘LIMIGA QAYTDINGIZ,MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇",
        'reply_markup'=>$foydali,
    ]);
}
    
if ($text == "💾QR-Kod"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n SIZ QR-KOD BO‘LIMIDASIZ, MENYUDAN O‘ZINGIZGA KERAKLI BO‘LIMNI TANLANG👇",
        'reply_markup'=>$qrkod,
    ]);
}

if($text=='/qr'){
bot('sendmessage',[
'chat_id'=>$chat_id,
    'text'=>"QR Kod yasashuchun 

`/qr Salom` 

Shu ko'rinishda yuboring" ,
'parse_mode'=>'markdown',
]);
}

if($text=='💾QR-Kod yasash'){
bot('sendmessage',[
'chat_id'=>$chat_id,
    'text'=>"QR Kod yaratish uchun 

`/qr Salom` 

Shu ko'rinishda yuboring" ,
'parse_mode'=>'markdown',
]);
}
if(mb_stripos($text,"/qr")!==false){ 
$ex=explode("/qr ",$text); 
$text=$ex[1]; 
$api = array("http://qr-code.ir/api/qr-code?s=5&e=M&t=P&d=$text","http://api.qrserver.com/v1/create-qr-code/?data=$text"); 
bot('sendPhoto',[
'chat_id'=>$chat_id,
"photo"=>$api[0],
    'caption'=>"🤖$botuser tomonidan tayyorlandi! 
Siz kiritgan matn QR kod rasmi\n \n Siz kiritgan tekst:  *$text*\n\n$reklama" ,
'parse_mode'=>'markdown',
]);
}

if ($text == "💾QR-Kodni o‘qish"){
    bot('SendMessage',[
        'chat_id'=>$chat_id,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Hurmatli $name,\n\n 🧾 QR kod ni o'qish uchun rasmni yuboring!!!",
        'reply_markup'=>$qrkod,
    ]);
}

$photo = $message->photo;
if($photo){
$file_id = $message->photo[0]->file_id;
$url = json_decode(file_get_contents('https://api.telegram.org/bot'.API_KEY.'/getFile?file_id='.$file_id),true);
$path=$url['result']['file_path'];
$file = 'https://api.telegram.org/file/bot'.API_KEY.'/'.$path;
$type = strtolower(strrchr($file,'.')); 
$type=str_replace('.','',$type);
if( ($type !== "png") and ($type !== "jpg")){
	bot('sendmessage',[
    'chat_id'=>$chat_id, 
    'text'=>"Xatolik #1 -> Fayl kengaytmasi .jpg yoki .png bo'lgan rasm yuboring" ,
]);
}else{
$okey = file_put_contents("data/$chat_id.png",file_get_contents($file));
if($okey==false){
	bot('sendmessage',[
    'chat_id'=>$chat_id, 
    'text'=>"Xatolik #2 -> Iltimos shu xabarni @iCoderNet ga yuboring" ,
]);
}else{
$url = "http://u3551.xvest1.ru/QR/data/$chat_id.png";
$api = json_decode(file_get_contents("https://api.qrserver.com/v1/read-qr-code/?fileurl=$url"));
$text=$api[0]->symbol[0]->data;
$error=$api[0]->symbol[0]->error;
if($error==null){
bot('sendmessage',[
'chat_id'=>$chat_id,
    'text'=>"🔣QR KODdagi Matn:⤵️

 `$text`

🎯By:$botuser" ,
'parse_mode'=>'markdown',
]);
}else{
bot('sendmessage',[
    'chat_id'=>$chat_id, 
    'text'=>"Xatolik #2 -> Uzur QR Kodni o'qib bo'lmadi" ,
]);
}
}
}
}




// ADMIN PANEL

$admpan = json_encode([
    'resize_keyboard'=>true,
'keyboard'=>[
[['text'=>"📊 Statistika"],['text'=>"📫Pochta tizimi"]],[['text'=>"📁 Bot kodi"]],
[['text'=>"⬅️ Orqaga"]],
]
]);

if ($text == "⬅️ Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$admin,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Admin siz asosiy menyudasiz!" ,
        'reply_markup'=>$asosiy,
    ]);
}

$pochta = json_encode([
    'resize_keyboard'=>true,
'keyboard'=>[
[['text'=>"📝 Oddiy xabar"],['text'=>"🗑O‘chirish mumkin bo‘lgan xabar"]], 
[['text'=>"🗑 Orqaga"]],
]
]);

if ($text == "🗑 Orqaga"){
    bot('SendMessage',[
        'chat_id'=>$admin,
        'message_id'=>$messaga_id,
        'parse_mode'=>"html",
        'text'=>"Admin siz asosiy admin menyusidasiz!" ,
        'reply_markup'=>$admpan,
    ]);
}

if($text=="📫Pochta tizimi"){
if($chat_id==$admin){
	bot('sendMessage',[
	'chat_id'=>$admin,
	'text'=>"<b>👨‍💻Xurmatli Admin, 📫Pochta tizimiga xush kelibsiz.</b>",
	'parse_mode'=>"html",
	'reply_markup'=>$pochta,
]);
}
} 

if($text=="/panel"){
if($chat_id==$admin){
	bot('sendMessage',[
	'chat_id'=>$admin,
	'text'=>"<b>👨‍💻Admin paneliga xush kelibsiz.</b>",
	'parse_mode'=>"html",
	'reply_markup'=>$admpan,
]);
}else{
bot('sendMessage',[
	'chat_id'=>$chat_id,
	'text'=>"<b>🚫 Ushbu bo'lim siz uchun emas.</b>",
	'parse_mode'=>"html",
	'reply_markup'=>$asosiy,
]);
}
}
 $yubor1=file_get_contents("yubor.txt");
if($text == "📝 Oddiy xabar" and $chat_id == $admin){
$lichka=file_get_contents("stat/stat.txt");
$lich=substr_count($lichka,"n");
bot('deleteMessage',[
'chat_id'=>$admin,
'message_id'=>$message_id,
]);
bot('sendMessage',[
'chat_id'=>$admin,
'text'=>"<b>🤖: $botuser\n
👥Jami obunachilar:  $stat
🙌Halol bo‘l va yana bir narsani unutma: Obunachilaring puldan ustun\n
Xabar matnini yuboring:</b>",
'parse_mode'=>'html',
]); 
file_put_contents("yubor.txt","sendpost");
}
if($yubor1=="sendpost" and $idi == $admin){
unlink("yubor.txt");
bot('sendMessage',[
'chat_id'=>$chat_id,
'text'=>"<b>↗️ Foydalanuvchilarga xabar yuborish boshlandi.</b>",
"parse_mode"=>"html",
]);
$x=0;
$y=0;
$lich = file_get_contents("stat/stat.txt");
$lichim = substr_count($lich,"n");
$lichka = explode("n",$lich);
foreach($lichka as $lichkalar){
$ok=bot('sendmessage',[
 'chat_id'=>$lichkalar,
 'text'=>"<b>$text</b>",
'parse_mode'=>'html',
json_encode([
'inline_keyboard'=>[
[['text'=>"",'url'=>"tg://user?id=$admin"]],
]
]),
])->ok;
if($ok==true){
$y=$y+1;
bot('editmessagetext',[
'chat_id'=>$chat_id,
'text'=>"<b>✅️ Xabar yuborildi: $y ta

❌️ Xabar yuborilmadi: $x ta</b>",
'message_id'=>$message_id+1,
'parse_mode'=>'html',
]);
}else{

$x=$x+1;
bot('editmessagetext',[
'chat_id'=>$chat_id,
'text'=>"<b>✅️ Xabar yuborildi: $y ta

❌️ Xabar yuborilmadi: $x ta</b>",
'message_id'=>$message_id+1,
'parse_mode'=>'html',
]);
}
}
bot('deletemessage',[
'chat_id'=>$chat_id,
'message_id'=>$message_id+1,
]);
bot('sendMessage',[
  'chat_id'=>$chat_id,
  'text'=>"<b>✅️ Xabar yuborildi: $y ta

❌️ Xabar yuborilmadi: $x ta</b>",
'parse_mode'=>'html',
"reply_markup"=>$pochta,
  ]);
}

$xabar1=file_get_contents("xabar.txt");
if($text == "🗑O‘chirish mumkin bo‘lgan xabar" and $chat_id == $admin){
$lichka=file_get_contents("stat/stat.txt");
$lich=substr_count($lichka,"n");
bot('deleteMessage',[
'chat_id'=>$admin,
'message_id'=>$message_id,
]);
bot('sendMessage',[
'chat_id'=>$admin,
'text'=>"<b>🤖: $botuser\n
👥Jami obunachilar:  $stat
🙌Halol bo‘l va yana bir narsani unutma: Obunachilaring puldan ustun\n
Xabar matnini yuboring:</b>",
'parse_mode'=>'html',
]); 
file_put_contents("xabar.txt","sendpost");
}
if($xabar1=="sendpost" and $idi == $admin){
unlink("xabar.txt");
bot('sendMessage',[
'chat_id'=>$chat_id,
'text'=>"<b>↗️ Foydalanuvchilarga xabar yuborish boshlandi.</b>",
"parse_mode"=>"html",
]);
$x=0;
$y=0;
$lich = file_get_contents("stat/stat.txt");
$lichim = substr_count($lich,"n");
$lichka = explode("n",$lich);
foreach($lichka as $lichkalar){
$ok=bot('sendmessage',[
 'chat_id'=>$lichkalar,
 'text'=>"<b>$text</b>",
'parse_mode'=>'html',
'reply_markup'=>$ochir,
])->ok;
if($ok==true){
$y=$y+1;
bot('editmessagetext',[
'chat_id'=>$chat_id,
'text'=>"<b>✅️ Xabar yuborildi: $y ta

❌️ Xabar yuborilmadi: $x ta</b>",
'message_id'=>$message_id+1,
'parse_mode'=>'html',
]);
}else{

$x=$x+1;
bot('editmessagetext',[
'chat_id'=>$chat_id,
'text'=>"<b>✅️ Xabar yuborildi: $y ta

❌️ Xabar yuborilmadi: $x ta</b>",
'message_id'=>$message_id+1,
'parse_mode'=>'html',
]);
}
}
bot('deletemessage',[
'chat_id'=>$chat_id,
'message_id'=>$message_id+1,
]);
bot('sendMessage',[
  'chat_id'=>$chat_id,
  'text'=>"<b>✅️ Xabar yuborildi: $y ta

❌️ Xabar yuborilmadi: $x ta</b>",
'parse_mode'=>'html',
"reply_markup"=>$pochta, 
  ]);
}



if($text == "📊 Statistika"){
   bot('sendMessage',[
   'chat_id'=>$admin,
    'text'=>"<b>🤖$botuser 
📊 Bot statistikasi

👤 A'zolar: $stat ta

📅 Sana: $sana
⌚️Soat: $time 
🤵‍♂Admin: $adminuser

⚡️Bot ochilgan sana: $opened
📌Bot ochilganiga: $boldi</b>",
'parse_mode'=>'html',
 ]);
 }

if($text == "📁 Bot kodi")
            if($chat_id == $admin){
        bot('sendDocument',[
        'chat_id'=>$admin,
        'document'=>new CURLFile(__FILE__),
        'caption'=>"<b>$botuser kodi</b>",
        'parse_mode'=>'html',
        ]);
        }else{
            bot('SendMessage',[
            'chat_id'=>$chat_id,
            'text'=>"⚠️ Bu kod faqat Adminlar uchun!",
            'parse_mode'=>"html",
            ]);
            }
