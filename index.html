import { useState, useEffect, useRef } from "react";

const C = {
  bg:"#0C0C0D", surface:"#161618", surfaceMid:"#1E1E21",
  surfaceHigh:"#272729", border:"#26262A", borderLight:"#303035",
  gold:"#F5C842", goldDim:"#C9A030", goldFaint:"#211C06",
  amber:"#F09830", red:"#FF4757", redFaint:"#280B0D",
  green:"#2ED573", greenFaint:"#0B2217",
  blue:"#4F8EF7", blueFaint:"#0D1A38",
  purple:"#B44FE8", text:"#EDECEA",
  textSec:"#8A8A9A", textMuted:"#52525E",
};

const iqd = (n) => `${Number(n).toLocaleString("ar-IQ")} د.ع`;

const T = {
  en:{
    dir:"ltr", appName:"CutPro",
    nav:{ dashboard:"Dashboard", bookings:"Bookings", customers:"Customers",
          services:"Services", finance:"Finance", notifications:"Alerts",
          settings:"Settings", barbers:"Barbers", bookingPage:"Booking Page" },
    dash:{ greeting:"Good morning", revenue:"Revenue", appts:"Appointments",
           customers:"Customers", weeklyRevenue:"Weekly Revenue",
           upcomingLabel:"Confirmed", pendingLabel:"Needs action",
           cancelRate:"Cancel Rate", popularService:"Top Service", waMessages:"WhatsApp msgs" },
    book:{ title:"Bookings", newBooking:"New Booking",
           filter_all:"All", filter_confirmed:"Confirmed", filter_pending:"Pending",
           filter_completed:"Done", filter_cancelled:"Cancelled",
           accept:"Accept", reject:"Reject",
           noAppts:"No appointments yet", bookFirst:"Create your first booking" },
    modal:{ selectCustomer:"Select Customer", selectService:"Select Service",
            selectBarber:"Select Barber", selectDate:"Date", selectTime:"Time",
            paymentMethod:"Payment", cash:"Cash", online:"Online", deposit:"Deposit",
            confirm:"Confirm Booking", cancel:"Cancel", notes:"Notes (optional)",
            depositAmt:"Deposit Amount" },
    customers:{ title:"Customers", search:"Search customers…", loyal:"Loyal",
                totalVisits:"Visits", totalSpent:"Total Spent",
                lastVisit:"Last visit", addCustomer:"Add Customer",
                noResults:"No customers found", phone:"Phone", notes:"Notes" },
    services:{ title:"Services", addService:"Add Service", name_en:"Name (EN)",
               name_ar:"Name (AR)", duration:"Duration (min)", price:"Price",
               save:"Save", cancel:"Cancel", edit:"Edit", delete:"Delete",
               noServices:"No services yet", addFirst:"Add your first service" },
    finance:{ title:"Finance", today:"Today", week:"Week", month:"Month",
              totalRevenue:"Total Revenue", cash:"Cash", online:"Online", deposit:"Deposit",
              transactions:"Transactions", dailyAvg:"Daily Avg", busiest:"Busiest Day",
              cancelRate:"Cancel Rate", peakHour:"Peak Hour", returnRate:"Return Rate" },
    notif:{ title:"Notifications", markAll:"Mark all read", empty:"All caught up ✓" },
    settings:{ title:"Settings", language:"Language", workHours:"Working Hours",
               from:"From", to:"To", cancellPolicy:"Cancellation Policy",
               channels:"Notification Channels", inApp:"In-App",
               whatsapp:"WhatsApp", sms:"SMS", email:"Email",
               save:"Save Changes", shopName:"Shop Name", phone:"Phone", address:"Address",
               profile:"Shop Profile", depositSettings:"Deposit Settings",
               depositType:"Deposit Type", noDeposit:"No Deposit",
               fixedDeposit:"Fixed Amount", percentDeposit:"Percentage",
               depositValue:"Value", multiBarber:"Multi-Barber Mode",
               whatsappConnect:"Connect WhatsApp", whatsappConnected:"WhatsApp Connected ✓",
               bookingLink:"Booking Page Link", copyLink:"Copy Link", linkCopied:"Copied!" },
    barbers:{ title:"Barbers", addBarber:"Add Barber", noBarbers:"No barbers yet",
              name:"Name", specialty:"Specialty" },
    status:{ confirmed:"Confirmed", pending:"Pending", completed:"Completed", cancelled:"Cancelled" },
    admin:{ title:"Super Admin", shops:"All Shops", addShop:"Add Shop",
            active:"Active", suspended:"Suspended", expiry:"Expiry",
            suspend:"Suspend", activate:"Activate", newShop:"New Shop",
            shopName:"Shop Name", ownerPhone:"Owner Phone", plan:"Plan" },
    mins:"min", ago:"ago", today:"Today", save:"Save", cancel:"Cancel", logout:"Sign out",
  },
  ar:{
    dir:"rtl", appName:"كت برو",
    nav:{ dashboard:"الرئيسية", bookings:"الحجوزات", customers:"العملاء",
          services:"الخدمات", finance:"المالية", notifications:"الإشعارات",
          settings:"الإعدادات", barbers:"الحلاقين", bookingPage:"صفحة الحجز" },
    dash:{ greeting:"صباح الخير", revenue:"الإيرادات", appts:"المواعيد",
           customers:"العملاء", weeklyRevenue:"إيرادات الأسبوع",
           upcomingLabel:"المؤكدة", pendingLabel:"تحتاج إجراء",
           cancelRate:"نسبة الإلغاء", popularService:"أشهر خدمة", waMessages:"رسائل واتساب" },
    book:{ title:"الحجوزات", newBooking:"حجز جديد",
           filter_all:"الكل", filter_confirmed:"مؤكد", filter_pending:"انتظار",
           filter_completed:"مكتمل", filter_cancelled:"ملغي",
           accept:"قبول", reject:"رفض",
           noAppts:"لا توجد مواعيد", bookFirst:"أنشئ أول حجز" },
    modal:{ selectCustomer:"اختر العميل", selectService:"اختر الخدمة",
            selectBarber:"اختر الحلاق", selectDate:"التاريخ", selectTime:"الوقت",
            paymentMethod:"الدفع", cash:"نقدي", online:"إلكتروني", deposit:"عربون",
            confirm:"تأكيد الحجز", cancel:"إلغاء", notes:"ملاحظات",
            depositAmt:"مبلغ العربون" },
    customers:{ title:"العملاء", search:"بحث عن عميل…", loyal:"وفي",
                totalVisits:"الزيارات", totalSpent:"إجمالي الإنفاق",
                lastVisit:"آخر زيارة", addCustomer:"إضافة عميل",
                noResults:"لا نتائج", phone:"الهاتف", notes:"ملاحظات" },
    services:{ title:"الخدمات", addService:"إضافة خدمة", name_en:"الاسم (EN)",
               name_ar:"الاسم (AR)", duration:"المدة (دقيقة)", price:"السعر",
               save:"حفظ", cancel:"إلغاء", edit:"تعديل", delete:"حذف",
               noServices:"لا توجد خدمات", addFirst:"أضف أول خدمة" },
    finance:{ title:"المالية", today:"اليوم", week:"الأسبوع", month:"الشهر",
              totalRevenue:"إجمالي الإيرادات", cash:"نقدي", online:"إلكتروني", deposit:"عربون",
              transactions:"المعاملات", dailyAvg:"المعدل اليومي", busiest:"أكثر يوم",
              cancelRate:"نسبة الإلغاء", peakHour:"ساعة الذروة", returnRate:"معدل العودة" },
    notif:{ title:"الإشعارات", markAll:"تحديد الكل كمقروء", empty:"لا توجد إشعارات ✓" },
    settings:{ title:"الإعدادات", language:"اللغة", workHours:"ساعات العمل",
               from:"من", to:"إلى", cancellPolicy:"سياسة الإلغاء",
               channels:"قنوات الإشعارات", inApp:"داخل التطبيق",
               whatsapp:"واتساب", sms:"رسائل قصيرة", email:"البريد",
               save:"حفظ التغييرات", shopName:"اسم المحل", phone:"الهاتف", address:"العنوان",
               profile:"ملف المحل", depositSettings:"إعدادات العربون",
               depositType:"نوع العربون", noDeposit:"بدون عربون",
               fixedDeposit:"مبلغ ثابت", percentDeposit:"نسبة مئوية",
               depositValue:"القيمة", multiBarber:"وضع متعدد الحلاقين",
               whatsappConnect:"ربط واتساب", whatsappConnected:"واتساب متصل ✓",
               bookingLink:"رابط صفحة الحجز", copyLink:"نسخ الرابط", linkCopied:"تم النسخ!" },
    barbers:{ title:"الحلاقين", addBarber:"إضافة حلاق", noBarbers:"لا يوجد حلاقين",
              name:"الاسم", specialty:"التخصص" },
    status:{ confirmed:"مؤكد", pending:"انتظار", completed:"مكتمل", cancelled:"ملغي" },
    admin:{ title:"لوحة المدير العام", shops:"جميع المحلات", addShop:"إضافة محل",
            active:"نشط", suspended:"موقوف", expiry:"انتهاء الاشتراك",
            suspend:"إيقاف", activate:"تفعيل", newShop:"محل جديد",
            shopName:"اسم المحل", ownerPhone:"هاتف المالك", plan:"الخطة" },
    mins:"دقيقة", ago:"مضت", today:"اليوم", save:"حفظ", cancel:"إلغاء", logout:"خروج",
  },
};

const CUSTOMERS = [
  { id:1, name:"Ali Al-Baghdadi",   nameAr:"علي البغدادي",    phone:"07701234567", visits:24, spent:480000, lastVisit:"اليوم",      loyal:true,  avatar:"ع", favService:"قص شعر",    notes:"يفضل بدون ماكينة" },
  { id:2, name:"Hassan Al-Mosuli",  nameAr:"حسن الموصلي",    phone:"07809876543", visits:18, spent:360000, lastVisit:"قبل 3 أيام", loyal:true,  avatar:"ح", favService:"تشذيب لحية", notes:"" },
  { id:3, name:"Kareem Salman",     nameAr:"كريم سلمان",     phone:"07712345678", visits:8,  spent:120000, lastVisit:"قبل أسبوع",  loyal:false, avatar:"ك", favService:"قص شعر",    notes:"" },
  { id:4, name:"Omar Fadhel",       nameAr:"عمر فاضل",       phone:"07901234567", visits:3,  spent:45000,  lastVisit:"قبل أسبوعين",loyal:false, avatar:"ع", favService:"حلاقة",     notes:"" },
  { id:5, name:"Mustafa Al-Tikrity",nameAr:"مصطفى التكريتي", phone:"07751234567", visits:31, spent:620000, lastVisit:"أمس",        loyal:true,  avatar:"م", favService:"قص شعر",    notes:"عميل VIP" },
  { id:6, name:"Zaid Al-Najafi",    nameAr:"زيد النجفي",     phone:"07721234567", visits:12, spent:192000, lastVisit:"قبل 4 أيام", loyal:false, avatar:"ز", favService:"عناية وجه",  notes:"" },
];
const SERVICES_INIT = [
  { id:1, name:"Haircut",     nameAr:"قص شعر",       duration:30, price:15000, color:C.gold   },
  { id:2, name:"Beard Trim",  nameAr:"تشذيب لحية",   duration:20, price:10000, color:C.amber  },
  { id:3, name:"Hair Color",  nameAr:"صباغة شعر",    duration:60, price:35000, color:C.blue   },
  { id:4, name:"Full Shave",  nameAr:"حلاقة كاملة",  duration:30, price:12000, color:C.green  },
  { id:5, name:"Facial Care", nameAr:"عناية وجه",    duration:45, price:25000, color:C.purple },
  { id:6, name:"Kids Cut",    nameAr:"قص أطفال",     duration:20, price:10000, color:C.red    },
];
const BARBERS_INIT = [
  { id:1, name:"أبو علي",    nameEn:"Abu Ali",      specialty:"قص وتشذيب",    avatar:"أ", color:C.gold,   bookings:24 },
  { id:2, name:"أستاذ حسن", nameEn:"Ustad Hassan", specialty:"صباغة وعناية", avatar:"ح", color:C.blue,   bookings:18 },
];
const APPTS_INIT = [
  { id:1, customerId:1, barberId:1, service:"قص شعر",      time:"09:00", duration:30, status:"confirmed", payment:"cash",    price:15000, note:"",                source:"app"          },
  { id:2, customerId:2, barberId:2, service:"صباغة شعر",   time:"10:00", duration:60, status:"confirmed", payment:"online",  price:35000, note:"أول مرة صباغة",  source:"whatsapp"     },
  { id:3, customerId:3, barberId:1, service:"حلاقة كاملة", time:"11:30", duration:30, status:"pending",   payment:"cash",    price:12000, note:"",                source:"whatsapp"     },
  { id:4, customerId:4, barberId:1, service:"قص شعر",      time:"13:00", duration:30, status:"confirmed", payment:"cash",    price:15000, note:"",                source:"app"          },
  { id:5, customerId:5, barberId:2, service:"تشذيب لحية",  time:"14:30", duration:20, status:"pending",   payment:"cash",    price:10000, note:"عميل منتظم",     source:"app"          },
  { id:6, customerId:6, barberId:1, service:"عناية وجه",   time:"16:00", duration:45, status:"confirmed", payment:"deposit", price:25000, note:"",                source:"booking_page" },
];
const NOTIFS_INIT = [
  { id:1, type:"whatsapp", text:"علي البغدادي طلب حجز قص شعر غداً الساعة 5 مساءً عبر واتساب",    textEn:"Ali Al-Baghdadi requested haircut tomorrow 5PM via WhatsApp", time:"2m",  read:false },
  { id:2, type:"booking",  text:"حسن الموصلي حجز صباغة شعر الساعة 10 صباحاً",                   textEn:"Hassan booked Hair Color at 10:00 AM",                        time:"15m", read:false },
  { id:3, type:"reminder", text:"موعد كريم سلمان بعد 30 دقيقة",                                  textEn:"Kareem Salman appointment in 30 minutes",                     time:"28m", read:false },
  { id:4, type:"payment",  text:"تم استلام دفعة 35,000 د.ع من حسن الموصلي",                      textEn:"Payment 35,000 IQD received from Hassan",                     time:"1h",  read:true  },
  { id:5, type:"system",   text:"التقرير الأسبوعي جاهز — 2,960,000 د.ع إجمالي",                 textEn:"Weekly report: 2,960,000 IQD total",                          time:"1d",  read:true  },
];
const ADMIN_SHOPS = [
  { id:1, name:"صالون أبو علي",  owner:"07701111111", plan:"Pro",   status:"active",    expiry:"2025-12-31", appts:248 },
  { id:2, name:"حلاقة الفارس",  owner:"07702222222", plan:"Basic", status:"active",    expiry:"2025-09-15", appts:134 },
  { id:3, name:"باربر الرشيد",  owner:"07703333333", plan:"Pro",   status:"suspended", expiry:"2025-06-01", appts:89  },
  { id:4, name:"ستايل البصرة",  owner:"07704444444", plan:"Basic", status:"active",    expiry:"2025-11-20", appts:201 },
];
const WEEKLY_REV  = [320000,410000,280000,520000,460000,390000,580000];
const PEAK_HOURS  = [2,4,8,12,15,9,11,6,3,1];
const DAYS_EN = ["Sun","Mon","Tue","Wed","Thu","Fri","Sat"];
const DAYS_AR = ["أحد","اثن","ثلا","أرب","خمي","جمع","سبت"];
const PEAK_LBL = ["9","10","11","12","1","2","3","4","5","6"];
const I = ({ n, s=20, c="currentColor", sw=2 }) => {
  const d = {
    home:     <><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></>,
    calendar: <><rect x="3" y="4" width="18" height="18" rx="2"/><line x1="16" y1="2" x2="16" y2="6"/><line x1="8" y1="2" x2="8" y2="6"/><line x1="3" y1="10" x2="21" y2="10"/></>,
    users:    <><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></>,
    scissors: <><circle cx="6" cy="6" r="3"/><circle cx="6" cy="18" r="3"/><line x1="20" y1="4" x2="8.12" y2="15.88"/><line x1="14.47" y1="14.48" x2="20" y2="20"/><line x1="8.12" y1="8.12" x2="12" y2="12"/></>,
    dollar:   <><line x1="12" y1="1" x2="12" y2="23"/><path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"/></>,
    settings: <><circle cx="12" cy="12" r="3"/><path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1-2.83 2.83l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-4 0v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83-2.83l.06-.06A1.65 1.65 0 0 0 4.68 15a1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1 0-4h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 2.83-2.83l.06.06A1.65 1.65 0 0 0 9 4.68a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 4 0v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 2.83l-.06.06A1.65 1.65 0 0 0 19.4 9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 0 4h-.09a1.65 1.65 0 0 0-1.51 1z"/></>,
    bell:     <><path d="M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9"/><path d="M13.73 21a2 2 0 0 1-3.46 0"/></>,
    check:    <><polyline points="20 6 9 17 4 12"/></>,
    x:        <><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></>,
    clock:    <><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></>,
    plus:     <><line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/></>,
    trend:    <><polyline points="23 6 13.5 15.5 8.5 10.5 1 18"/><polyline points="17 6 23 6 23 12"/></>,
    phone:    <><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 13.1 19.79 19.79 0 0 1 1.62 4.43 2 2 0 0 1 3.6 2.35h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L7.91 9.91a16 16 0 0 0 6.16 6.16l.91-1.9a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 21.73 16.92z"/></>,
    search:   <><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></>,
    edit:     <><path d="M11 4H4a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"/><path d="M18.5 2.5a2.121 2.121 0 0 1 3 3L12 15l-4 1 1-4 9.5-9.5z"/></>,
    trash:    <><polyline points="3 6 5 6 21 6"/><path d="M19 6v14a2 2 0 0 1-2 2H7a2 2 0 0 1-2-2V6m3 0V4a2 2 0 0 1 2-2h4a2 2 0 0 1 2 2v2"/></>,
    globe:    <><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></>,
    star:     <><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2" fill="currentColor"/></>,
    msg:      <><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/></>,
    copy:     <><rect x="9" y="9" width="13" height="13" rx="2"/><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"/></>,
    link:     <><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"/><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"/></>,
    shield:   <><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></>,
    info:     <><circle cx="12" cy="12" r="10"/><line x1="12" y1="16" x2="12" y2="12"/><line x1="12" y1="8" x2="12.01" y2="8"/></>,
  };
  if (n === "wa") return (
    <svg width={s} height={s} viewBox="0 0 24 24" fill={c}>
      <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/>
    </svg>
  );
  return <svg width={s} height={s} fill="none" stroke={c} strokeWidth={sw} strokeLinecap="round" strokeLinejoin="round" viewBox="0 0 24 24">{d[n]}</svg>;
};

const Av = ({ char, size=40, bg=C.gold }) => (
  <div style={{ width:size, height:size, borderRadius:"50%", flexShrink:0,
    background:`linear-gradient(135deg,${bg}22,${bg}40)`,
    border:`1.5px solid ${bg}55`, display:"flex", alignItems:"center",
    justifyContent:"center", color:bg, fontWeight:800, fontSize:size*0.38 }}>{char}</div>
);

const Badge = ({ status, t }) => {
  const m = { confirmed:{bg:"#0C2218",col:C.green}, pending:{bg:C.goldFaint,col:C.gold},
               completed:{bg:C.blueFaint,col:C.blue}, cancelled:{bg:C.redFaint,col:C.red} }[status]
    || {bg:C.goldFaint,col:C.gold};
  return <span style={{ background:m.bg, color:m.col, padding:"3px 10px",
    borderRadius:20, fontSize:11, fontWeight:700 }}>{t.status[status]||status}</span>;
};

const Toggle = ({ on, onChange }) => (
  <div onClick={()=>onChange(!on)} style={{ width:46, height:26, borderRadius:13,
    background:on?C.gold:C.surfaceHigh, position:"relative", cursor:"pointer",
    flexShrink:0, transition:"background .2s", border:`1px solid ${on?C.goldDim:C.border}` }}>
    <div style={{ position:"absolute", top:3, left:on?22:3, width:18, height:18,
      borderRadius:"50%", background:on?C.bg:C.textMuted,
      transition:"left .2s", boxShadow:"0 1px 4px #0006" }}/>
  </div>
);

const Pill = ({ active, onClick, children }) => (
  <button onClick={onClick} style={{ padding:"7px 15px", borderRadius:20, border:"none",
    cursor:"pointer", fontSize:12, fontWeight:700, whiteSpace:"nowrap",
    transition:"all .15s", fontFamily:"inherit",
    background:active?C.gold:C.surfaceHigh, color:active?C.bg:C.textSec }}>{children}</button>
);

const Inp = ({ label, value, onChange, type="text", placeholder="", readOnly=false }) => (
  <div style={{ marginBottom:14 }}>
    {label && <div style={{ color:C.textSec, fontSize:12, marginBottom:6, fontWeight:600 }}>{label}</div>}
    <input type={type} value={value} onChange={e=>onChange&&onChange(e.target.value)}
      placeholder={placeholder} readOnly={readOnly}
      style={{ width:"100%", background:C.surfaceMid, border:`1px solid ${C.border}`,
        borderRadius:11, padding:"11px 14px", color:readOnly?C.textSec:C.text, fontSize:14,
        outline:"none", boxSizing:"border-box", fontFamily:"inherit" }}
      onFocus={e=>{ if(!readOnly) e.target.style.borderColor=C.gold; }}
      onBlur={e=>{ e.target.style.borderColor=C.border; }}/>
  </div>
);

const Sel = ({ label, value, onChange, options }) => (
  <div style={{ marginBottom:14 }}>
    {label && <div style={{ color:C.textSec, fontSize:12, marginBottom:6, fontWeight:600 }}>{label}</div>}
    <select value={value} onChange={e=>onChange(e.target.value)}
      style={{ width:"100%", background:C.surfaceMid, border:`1px solid ${C.border}`,
        borderRadius:11, padding:"11px 14px", color:C.text, fontSize:14,
        outline:"none", boxSizing:"border-box", fontFamily:"inherit",
        cursor:"pointer", appearance:"none" }}>
      {options.map(o=><option key={o.v} value={o.v}>{o.l}</option>)}
    </select>
  </div>
);

const Card = ({ children, style={} }) => (
  <div style={{ background:C.surface, border:`1px solid ${C.border}`,
    borderRadius:18, padding:20, ...style }}>{children}</div>
);

const Btn = ({ children, onClick, v="primary", style={}, disabled=false, full=false }) => {
  const vs = { primary:{bg:C.gold,col:C.bg}, ghost:{bg:C.surfaceHigh,col:C.textSec},
               danger:{bg:C.redFaint,col:C.red}, success:{bg:C.greenFaint,col:C.green},
               blue:{bg:C.blueFaint,col:C.blue} }[v];
  return <button onClick={onClick} disabled={disabled} style={{ background:vs.bg, color:vs.col,
    border:"none", borderRadius:11, padding:"11px 18px", fontWeight:700, fontSize:14,
    cursor:disabled?"not-allowed":"pointer", fontFamily:"inherit",
    opacity:disabled?0.5:1, transition:"opacity .15s, transform .1s",
    width:full?"100%":"auto", ...style }}
    onMouseDown={e=>{ if(!disabled) e.currentTarget.style.transform="scale(0.97)"; }}
    onMouseUp={e=>{ e.currentTarget.style.transform="scale(1)"; }}>{children}</button>;
};

const EmptyState = ({ icon, title, sub, action }) => (
  <div style={{ textAlign:"center", padding:"52px 20px" }}>
    <div style={{ width:72, height:72, borderRadius:20, background:C.surfaceHigh,
      display:"flex", alignItems:"center", justifyContent:"center", margin:"0 auto 16px" }}>
      <I n={icon} s={32} c={C.textMuted}/>
    </div>
    <div style={{ fontWeight:800, color:C.textSec, fontSize:17, marginBottom:6 }}>{title}</div>
    {sub && <div style={{ color:C.textMuted, fontSize:14, marginBottom:20 }}>{sub}</div>}
    {action}
  </div>
);

const StatCard = ({ icon, label, value, sub, color=C.gold, wide=false }) => (
  <div style={{ background:C.surface, border:`1px solid ${C.border}`, borderRadius:16,
    padding:"16px 16px", position:"relative", overflow:"hidden",
    gridColumn:wide?"1 / -1":"span 1" }}>
    <div style={{ position:"absolute", top:-10, right:-10, width:70, height:70,
      background:`radial-gradient(circle,${color}18,transparent 70%)` }}/>
    <div style={{ display:"flex", alignItems:"center", gap:8, marginBottom:10 }}>
      <div style={{ width:32, height:32, borderRadius:9, background:`${color}20`,
        display:"flex", alignItems:"center", justifyContent:"center", flexShrink:0 }}>
        <I n={icon} s={15} c={color}/>
      </div>
      <span style={{ color:C.textSec, fontSize:12, fontWeight:600 }}>{label}</span>
    </div>
    <div style={{ fontSize:19, fontWeight:900, color:C.text, letterSpacing:"-0.02em",
      lineHeight:1.2, wordBreak:"break-word" }}>{value}</div>
    {sub && <div style={{ fontSize:11, color:C.textMuted, marginTop:5 }}>{sub}</div>}
  </div>
);

const BarChart = ({ data, labels, hl=-1 }) => {
  const mx = Math.max(...data);
  return (
    <div style={{ display:"flex", alignItems:"flex-end", gap:5, height:80 }}>
      {data.map((v,i)=>(
        <div key={i} style={{ flex:1, display:"flex", flexDirection:"column", alignItems:"center", gap:4 }}>
          <div style={{ width:"100%", borderRadius:"4px 4px 0 0",
            height:`${(v/mx)*64}px`,
            background:(hl===-1&&i===data.length-1)||i===hl?C.gold:`${C.gold}33`,
            transition:"height .6s ease" }}/>
          <span style={{ fontSize:10, color:C.textMuted }}>{labels[i]}</span>
        </div>
      ))}
    </div>
  );
};

const SparkPie = ({ value, color=C.gold, size=52 }) => {
  const r=20, cx=26, cy=26, circ=2*Math.PI*r;
  const dash=(Math.min(100,Math.max(0,value))/100)*circ;
  return (
    <svg width={size} height={size} viewBox="0 0 52 52">
      <circle cx={cx} cy={cy} r={r} fill="none" stroke={`${color}22`} strokeWidth={6}/>
      <circle cx={cx} cy={cy} r={r} fill="none" stroke={color} strokeWidth={6}
        strokeDasharray={`${dash} ${circ-dash}`}
        strokeDashoffset={circ*0.25} strokeLinecap="round"/>
      <text x={cx} y={cy+5} textAnchor="middle" fill={color} fontSize="11" fontWeight="800">{value}%</text>
    </svg>
  );
};

const Toast = ({ msg, type="success", onClose }) => {
  const col = type==="success"?C.green:type==="error"?C.red:C.gold;
  return (
    <div style={{ position:"fixed", bottom:88, left:"50%", transform:"translateX(-50%)",
      background:C.surfaceHigh, border:`1px solid ${col}44`, borderRadius:14,
      padding:"12px 18px", zIndex:2000, display:"flex", alignItems:"center", gap:10,
      maxWidth:320, width:"calc(100% - 32px)", boxShadow:"0 8px 32px #000b",
      animation:"toastIn .3s ease" }}>
      <div style={{ width:8, height:8, borderRadius:"50%", background:col, flexShrink:0 }}/>
      <span style={{ color:C.text, fontSize:14, flex:1 }}>{msg}</span>
      <button onClick={onClose} style={{ background:"none", border:"none", color:C.textMuted, cursor:"pointer" }}>
        <I n="x" s={14} c={C.textMuted}/>
      </button>
    </div>
  );
};

const Modal = ({ open, onClose, title, children }) => {
  if (!open) return null;
  return (
    <div onClick={onClose} style={{ position:"fixed", inset:0, background:"#000c",
      zIndex:1500, display:"flex", alignItems:"flex-end", justifyContent:"center",
      animation:"fadeIn .2s ease" }}>
      <div onClick={e=>e.stopPropagation()} style={{ background:C.surface,
        borderRadius:"24px 24px 0 0", width:"100%", maxWidth:540, maxHeight:"92vh",
        overflow:"hidden", display:"flex", flexDirection:"column",
        border:`1px solid ${C.border}`, borderBottom:"none", animation:"slideUp .3s ease" }}>
        <div style={{ display:"flex", justifyContent:"center", padding:"12px 0 0" }}>
          <div style={{ width:40, height:4, borderRadius:2, background:C.borderLight }}/>
        </div>
        <div style={{ display:"flex", alignItems:"center", justifyContent:"space-between",
          padding:"14px 22px 0" }}>
          <div style={{ fontWeight:800, fontSize:17, color:C.text }}>{title}</div>
          <button onClick={onClose} style={{ background:C.surfaceHigh, border:"none",
            borderRadius:8, width:32, height:32, cursor:"pointer",
            display:"flex", alignItems:"center", justifyContent:"center" }}>
            <I n="x" s={15} c={C.textSec}/>
          </button>
        </div>
        <div style={{ overflowY:"auto", padding:"16px 22px 36px" }}>{children}</div>
      </div>
    </div>
  );
};
const ApptRow = ({ appt, customers, barbers, onAccept, onReject, t }) => {
  const cust = customers.find(c=>c.id===appt.customerId);
  const barb = barbers?.find(b=>b.id===appt.barberId);
  const name = cust?(t.dir==="rtl"?cust.nameAr:cust.name):"—";
  const srcCol = appt.source==="whatsapp"?C.green:appt.source==="booking_page"?C.blue:C.textMuted;
  const srcIcon = appt.source==="whatsapp"?"wa":appt.source==="booking_page"?"globe":"calendar";
  return (
    <div style={{ background:C.surface,
      border:`1px solid ${appt.status==="pending"?C.gold+"55":C.border}`,
      borderRadius:14, padding:"12px 14px", display:"flex", alignItems:"center", gap:10 }}>
      <Av char={cust?cust.avatar:"?"} size={40} bg={appt.status==="confirmed"?C.gold:C.textSec}/>
      <div style={{ flex:1, minWidth:0 }}>
        <div style={{ display:"flex", alignItems:"center", gap:5, flexWrap:"wrap" }}>
          <span style={{ fontWeight:700, color:C.text, fontSize:14 }}>{name}</span>
          <I n={srcIcon} s={10} c={srcCol}/>
        </div>
        <div style={{ color:C.textSec, fontSize:12, display:"flex", gap:6, flexWrap:"wrap", marginTop:2 }}>
          <span style={{ display:"flex", alignItems:"center", gap:3 }}>
            <I n="clock" s={10} c={C.textMuted}/>{appt.time}
          </span>
          <span>·</span><span>{appt.service}</span>
          {barb&&<><span>·</span><span style={{ color:C.gold }}>{t.dir==="rtl"?barb.name:barb.nameEn}</span></>}
        </div>
      </div>
      <div style={{ display:"flex", flexDirection:"column", alignItems:"flex-end", gap:5 }}>
        <Badge status={appt.status} t={t}/>
        <span style={{ color:C.gold, fontWeight:800, fontSize:13 }}>{iqd(appt.price)}</span>
      </div>
      {appt.status==="pending"&&(
        <div style={{ display:"flex", flexDirection:"column", gap:5 }}>
          <button onClick={()=>onAccept(appt.id)} style={{ width:30, height:30, borderRadius:8,
            border:"none", cursor:"pointer", background:`${C.green}22`,
            display:"flex", alignItems:"center", justifyContent:"center" }}>
            <I n="check" s={14} c={C.green}/>
          </button>
          <button onClick={()=>onReject(appt.id)} style={{ width:30, height:30, borderRadius:8,
            border:"none", cursor:"pointer", background:`${C.red}22`,
            display:"flex", alignItems:"center", justifyContent:"center" }}>
            <I n="x" s={14} c={C.red}/>
          </button>
        </div>
      )}
    </div>
  );
};

const BookingModal = ({ open, onClose, customers, services, barbers, onSave, t, depSet }) => {
  const [cId,setCId]=useState(""); const [sId,setSId]=useState("");
  const [bId,setBId]=useState(""); const [date,setDate]=useState(new Date().toISOString().split("T")[0]);
  const [time,setTime]=useState("09:00"); const [pay,setPay]=useState("cash");
  const [note,setNote]=useState("");
  const reset=()=>{ setCId("");setSId("");setBId("");setDate(new Date().toISOString().split("T")[0]);setTime("09:00");setPay("cash");setNote(""); };
  const svc=services.find(s=>s.id===Number(sId));
  const cust=customers.find(c=>c.id===Number(cId));
  const depAmt=()=>{ if(!svc||depSet.type==="none") return 0;
    return depSet.type==="fixed"?depSet.value:Math.round(svc.price*(depSet.value/100)); };
  const handleSave=()=>{ if(!cId||!sId) return;
    onSave({ id:Date.now(), customerId:Number(cId), barberId:Number(bId)||1,
      service:svc.nameAr, time, duration:svc.duration, status:"pending",
      payment:pay, price:svc.price, note, source:"app" });
    reset(); onClose(); };
  return (
    <Modal open={open} onClose={()=>{ reset();onClose(); }} title={t.book.newBooking}>
      <Sel label={t.modal.selectCustomer} value={cId} onChange={setCId}
        options={[{v:"",l:"— "+t.modal.selectCustomer+" —"},
          ...customers.map(c=>({v:String(c.id),l:t.dir==="rtl"?c.nameAr:c.name}))]}/>
      <Sel label={t.modal.selectService} value={sId} onChange={setSId}
        options={[{v:"",l:"— "+t.modal.selectService+" —"},
          ...services.map(s=>({v:String(s.id),l:(t.dir==="rtl"?s.nameAr:s.name)+` — ${iqd(s.price)}`}))]}/>
      {barbers.length>1&&<Sel label={t.modal.selectBarber} value={bId} onChange={setBId}
        options={[{v:"",l:"— "+t.modal.selectBarber+" —"},
          ...barbers.map(b=>({v:String(b.id),l:t.dir==="rtl"?b.name:b.nameEn}))]}/>}
      <div style={{ display:"flex", gap:12 }}>
        <div style={{ flex:1 }}><Inp label={t.modal.selectDate} value={date} onChange={setDate} type="date"/></div>
        <div style={{ flex:1 }}><Inp label={t.modal.selectTime} value={time} onChange={setTime} type="time"/></div>
      </div>
      <div style={{ marginBottom:14 }}>
        <div style={{ color:C.textSec, fontSize:12, marginBottom:8, fontWeight:600 }}>{t.modal.paymentMethod}</div>
        <div style={{ display:"flex", gap:8 }}>
          {[["cash",t.modal.cash],["online",t.modal.online],["deposit",t.modal.deposit]].map(([v,l])=>(
            <button key={v} onClick={()=>setPay(v)} style={{ flex:1, padding:"10px", borderRadius:10,
              fontFamily:"inherit", border:`1.5px solid ${pay===v?C.gold:C.border}`,
              background:pay===v?C.goldFaint:C.surfaceMid,
              color:pay===v?C.gold:C.textSec, fontWeight:700, fontSize:13, cursor:"pointer" }}>{l}</button>
          ))}
        </div>
      </div>
      <Inp label={t.modal.notes} value={note} onChange={setNote} placeholder="…"/>
      {cust&&svc&&(
        <div style={{ background:C.goldFaint, border:`1px solid ${C.gold}33`,
          borderRadius:12, padding:"12px 16px", marginBottom:16 }}>
          <div style={{ display:"flex", justifyContent:"space-between", marginBottom:4 }}>
            <span style={{ color:C.textSec, fontSize:13 }}>{t.dir==="rtl"?cust.nameAr:cust.name}</span>
            <span style={{ color:C.gold, fontWeight:800 }}>{iqd(svc.price)}</span>
          </div>
          <div style={{ color:C.textMuted, fontSize:12 }}>
            {t.dir==="rtl"?svc.nameAr:svc.name} · {time} · {svc.duration} {t.mins}
          </div>
          {depSet.type!=="none"&&<div style={{ color:C.amber, fontSize:12, marginTop:4 }}>
            {t.modal.depositAmt}: {iqd(depAmt())}
          </div>}
        </div>
      )}
      <div style={{ display:"flex", gap:10 }}>
        <Btn onClick={()=>{ reset();onClose(); }} v="ghost" style={{ flex:1 }}>{t.modal.cancel}</Btn>
        <Btn onClick={handleSave} disabled={!cId||!sId} style={{ flex:2 }}>{t.modal.confirm}</Btn>
      </div>
    </Modal>
  );
};

const PublicBookingPage = ({ services, barbers, onClose, shopName, lang }) => {
  const [step,setStep]=useState(1);
  const [sId,setSId]=useState(null); const [bId,setBId]=useState(null);
  const [date,setDate]=useState(""); const [time,setTime]=useState("");
  const [phone,setPhone]=useState(""); const [name_,setName]=useState("");
  const [confirmed,setConfirmed]=useState(false);
  const isRtl=lang==="ar";
  const svc=services.find(s=>s.id===sId);
  const barb=barbers.find(b=>b.id===bId);
  const TIMES=["09:00","09:30","10:00","10:30","11:00","11:30","13:00","13:30","14:00","14:30","15:00","16:00","16:30","17:00"];
  const lbl=(ar,en)=>isRtl?ar:en;

  return (
    <div style={{ position:"fixed", inset:0, background:C.bg, zIndex:3000, overflowY:"auto",
      direction:isRtl?"rtl":"ltr", fontFamily:"'Inter',-apple-system,sans-serif" }}>
      {/* Header */}
      <div style={{ background:C.surface, borderBottom:`1px solid ${C.border}`,
        padding:"14px 18px", display:"flex", alignItems:"center", justifyContent:"space-between",
        position:"sticky", top:0, zIndex:10 }}>
        <div style={{ display:"flex", alignItems:"center", gap:10 }}>
          <div style={{ width:36, height:36, borderRadius:10, background:`${C.gold}18`,
            border:`1px solid ${C.gold}33`, display:"flex", alignItems:"center", justifyContent:"center" }}>
            <I n="scissors" s={18} c={C.gold}/>
          </div>
          <div>
            <div style={{ fontWeight:900, fontSize:16, color:C.text }}>{shopName}</div>
            <div style={{ color:C.textSec, fontSize:11 }}>{lbl("احجز موعدك الآن","Book your appointment")}</div>
          </div>
        </div>
        <button onClick={onClose} style={{ background:C.surfaceHigh, border:"none",
          borderRadius:10, width:34, height:34, cursor:"pointer",
          display:"flex", alignItems:"center", justifyContent:"center" }}>
          <I n="x" s={17} c={C.textSec}/>
        </button>
      </div>

      {/* Step progress */}
      <div style={{ display:"flex", gap:4, padding:"14px 18px 0" }}>
        {[1,2,3,4].map(n=>(
          <div key={n} style={{ flex:1, height:4, borderRadius:2,
            background:n<=step?C.gold:C.surfaceHigh, transition:"background .3s" }}/>
        ))}
      </div>

      <div style={{ padding:"18px 18px 100px", maxWidth:480, margin:"0 auto" }}>

        {/* STEP 1 — اختر الخدمة */}
        {step===1&&(
          <div style={{ animation:"fadeIn .3s ease" }}>
            <div style={{ fontWeight:800, fontSize:20, color:C.text, marginBottom:4 }}>
              {lbl("اختر الخدمة","Choose a service")}
            </div>
            <div style={{ color:C.textSec, fontSize:14, marginBottom:18 }}>
              {lbl("ما الخدمة التي تريدها؟","What would you like today?")}
            </div>
            {services.map(s=>(
              <div key={s.id} onClick={()=>{ setSId(s.id); setStep(2); }}
                style={{ background:sId===s.id?C.goldFaint:C.surface,
                  border:`1.5px solid ${sId===s.id?C.gold:C.border}`,
                  borderRadius:16, padding:"15px", marginBottom:10, cursor:"pointer",
                  display:"flex", alignItems:"center", gap:14, transition:"all .15s" }}>
                <div style={{ width:46, height:46, borderRadius:13, background:`${s.color}18`,
                  display:"flex", alignItems:"center", justifyContent:"center", flexShrink:0 }}>
                  <I n="scissors" s={20} c={s.color}/>
                </div>
                <div style={{ flex:1 }}>
                  <div style={{ fontWeight:700, color:C.text, fontSize:15 }}>{isRtl?s.nameAr:s.name}</div>
                  <div style={{ color:C.textSec, fontSize:12, marginTop:3, display:"flex", alignItems:"center", gap:4 }}>
                    <I n="clock" s={11} c={C.textMuted}/>{s.duration} {lbl("دقيقة","min")}
                  </div>
                </div>
                <div style={{ fontWeight:900, color:s.color, fontSize:16 }}>{iqd(s.price)}</div>
              </div>
            ))}
          </div>
        )}

        {/* STEP 2 — الحلاق + الوقت */}
        {step===2&&(
          <div style={{ animation:"fadeIn .3s ease" }}>
            <div style={{ fontWeight:800, fontSize:20, color:C.text, marginBottom:4 }}>
              {lbl("اختر الموعد","Pick a time")}
            </div>
            <div style={{ display:"flex", alignItems:"center", gap:8, marginBottom:18,
              background:C.goldFaint, border:`1px solid ${C.gold}33`,
              borderRadius:10, padding:"10px 14px" }}>
              <I n="scissors" s={14} c={C.gold}/>
              <span style={{ color:C.gold, fontWeight:700, fontSize:14 }}>
                {svc&&(isRtl?svc.nameAr:svc.name)} — {svc&&iqd(svc.price)}
              </span>
            </div>

            {barbers.length>1&&(
              <>
                <div style={{ color:C.textSec, fontSize:12, fontWeight:600, marginBottom:8 }}>
                  {lbl("اختر الحلاق","Choose your barber")}
                </div>
                <div style={{ display:"flex", gap:10, marginBottom:18 }}>
                  {barbers.map(b=>(
                    <div key={b.id} onClick={()=>setBId(b.id)}
                      style={{ flex:1, background:bId===b.id?C.goldFaint:C.surface,
                        border:`1.5px solid ${bId===b.id?C.gold:C.border}`,
                        borderRadius:14, padding:"14px 10px", cursor:"pointer",
                        textAlign:"center", transition:"all .15s" }}>
                      <Av char={b.avatar} size={38} bg={bId===b.id?C.gold:C.textSec}/>
                      <div style={{ fontWeight:700, color:C.text, fontSize:13, marginTop:8 }}>
                        {isRtl?b.name:b.nameEn}
                      </div>
                      <div style={{ color:C.textMuted, fontSize:11, marginTop:3 }}>{b.specialty}</div>
                    </div>
                  ))}
                </div>
              </>
            )}

            <Inp label={lbl("التاريخ","Date")} value={date} onChange={setDate} type="date"/>

            <div style={{ color:C.textSec, fontSize:12, fontWeight:600, marginBottom:10 }}>
              {lbl("الأوقات المتاحة","Available times")}
            </div>
            <div style={{ display:"grid", gridTemplateColumns:"repeat(4,1fr)", gap:8, marginBottom:18 }}>
              {TIMES.map(tm=>(
                <div key={tm} onClick={()=>setTime(tm)}
                  style={{ padding:"10px 4px", borderRadius:10, textAlign:"center", cursor:"pointer",
                    background:time===tm?C.gold:C.surfaceHigh,
                    color:time===tm?C.bg:C.textSec,
                    fontWeight:700, fontSize:13, transition:"all .15s" }}>{tm}</div>
              ))}
            </div>

            <div style={{ display:"flex", gap:10 }}>
              <Btn onClick={()=>setStep(1)} v="ghost" style={{ flex:1 }}>{lbl("رجوع","Back")}</Btn>
              <Btn onClick={()=>setStep(3)}
                disabled={!date||!time||(barbers.length>1&&!bId)} style={{ flex:2 }}>
                {lbl("التالي →","Continue →")}
              </Btn>
            </div>
          </div>
        )}

        {/* STEP 3 — بيانات العميل */}
        {step===3&&(
          <div style={{ animation:"fadeIn .3s ease" }}>
            <div style={{ fontWeight:800, fontSize:20, color:C.text, marginBottom:4 }}>
              {lbl("بياناتك","Your details")}
            </div>
            <div style={{ color:C.textSec, fontSize:14, marginBottom:18 }}>
              {lbl("خطوة أخيرة لتأكيد حجزك","One last step to confirm your booking")}
            </div>

            <Inp label={lbl("الاسم الكامل","Full name")} value={name_}
              onChange={setName} placeholder={lbl("علي أحمد","Ali Ahmed")}/>
            <Inp label={lbl("رقم الهاتف","Phone number")} value={phone}
              onChange={setPhone} placeholder="07XX XXX XXXX" type="tel"/>

            {/* ملخص الحجز */}
            <div style={{ background:C.surfaceMid, border:`1px solid ${C.border}`,
              borderRadius:14, padding:"14px 16px", marginBottom:18 }}>
              <div style={{ fontWeight:700, color:C.text, fontSize:14, marginBottom:12 }}>
                {lbl("ملخص الحجز","Booking Summary")}
              </div>
              {[
                [lbl("الخدمة","Service"), svc&&(isRtl?svc.nameAr:svc.name)],
                [lbl("التاريخ","Date"), date],
                [lbl("الوقت","Time"), time],
                barbers.length>1&&barb?[lbl("الحلاق","Barber"), isRtl?barb.name:barb.nameEn]:null,
              ].filter(Boolean).map(([k,v],i,arr)=>(
                <div key={i} style={{ display:"flex", justifyContent:"space-between",
                  padding:"7px 0", borderBottom:i<arr.length-1?`1px solid ${C.border}`:"none" }}>
                  <span style={{ color:C.textSec, fontSize:13 }}>{k}</span>
                  <span style={{ color:C.text, fontWeight:700, fontSize:13 }}>{v}</span>
                </div>
              ))}
              <div style={{ display:"flex", justifyContent:"space-between", marginTop:10,
                paddingTop:10, borderTop:`1px solid ${C.gold}33` }}>
                <span style={{ color:C.textSec, fontSize:14, fontWeight:600 }}>{lbl("المجموع","Total")}</span>
                <span style={{ color:C.gold, fontWeight:900, fontSize:18 }}>{svc&&iqd(svc.price)}</span>
              </div>
            </div>

            <div style={{ display:"flex", gap:10 }}>
              <Btn onClick={()=>setStep(2)} v="ghost" style={{ flex:1 }}>{lbl("رجوع","Back")}</Btn>
              <Btn onClick={()=>setStep(4)} disabled={!name_.trim()||!phone.trim()} style={{ flex:2 }}>
                {lbl("تأكيد الحجز ✓","Confirm Booking ✓")}
              </Btn>
            </div>
          </div>
        )}

        {/* STEP 4 — تأكيد */}
        {step===4&&(
          <div style={{ textAlign:"center", paddingTop:24, animation:"fadeIn .4s ease" }}>
            <div style={{ width:88, height:88, borderRadius:26, background:`${C.green}15`,
              border:`2px solid ${C.green}44`, display:"flex", alignItems:"center",
              justifyContent:"center", margin:"0 auto 20px",
              boxShadow:`0 0 40px ${C.green}22` }}>
              <I n="check" s={44} c={C.green} sw={2.5}/>
            </div>
            <div style={{ fontWeight:900, fontSize:24, color:C.text, marginBottom:10 }}>
              {lbl("تم تأكيد حجزك! ✓","Booking Confirmed! ✓")}
            </div>
            <div style={{ color:C.textSec, fontSize:14, marginBottom:8, lineHeight:1.6 }}>
              {lbl(
                `سيصلك تأكيد على واتساب على الرقم ${phone}`,
                `A WhatsApp confirmation will be sent to ${phone}`
              )}
            </div>
            <div style={{ display:"inline-flex", alignItems:"center", gap:6,
              background:"#0B2217", border:"1px solid #2ED57333", borderRadius:10,
              padding:"8px 14px", marginBottom:24 }}>
              <I n="wa" s={16} c={C.green}/>
              <span style={{ color:C.green, fontWeight:700, fontSize:13 }}>
                {lbl("رسالة واتساب في الطريق…","WhatsApp message on its way…")}
              </span>
            </div>

            <div style={{ background:C.surfaceMid, border:`1px solid ${C.border}`,
              borderRadius:14, padding:"14px 16px", marginBottom:24, textAlign:isRtl?"right":"left" }}>
              {[
                [lbl("الخدمة","Service"), svc&&(isRtl?svc.nameAr:svc.name)],
                [lbl("الموعد","Appointment"), `${date} — ${time}`],
                [lbl("السعر","Price"), svc&&iqd(svc.price)],
              ].map(([k,v],i,arr)=>(
                <div key={i} style={{ display:"flex", justifyContent:"space-between",
                  padding:"7px 0", borderBottom:i<arr.length-1?`1px solid ${C.border}`:"none" }}>
                  <span style={{ color:C.textSec, fontSize:13 }}>{k}</span>
                  <span style={{ color:i===2?C.gold:C.text, fontWeight:i===2?900:700 }}>{v}</span>
                </div>
              ))}
            </div>
            <Btn onClick={onClose} full style={{ padding:"14px" }}>
              {lbl("إغلاق","Close")}
            </Btn>
          </div>
        )}
      </div>
    </div>
  );
};

// ══════════════════════════════════════════════════════
//  WHATSAPP AI SIMULATOR PAGE
// ══════════════════════════════════════════════════════
const WhatsAppAIPage = ({ services, barbers, onClose, shopName, lang, onBookingCreated }) => {
  const isRtl=lang==="ar";
  const lbl=(ar,en)=>isRtl?ar:en;
  const [msgs,setMsgs]=useState([
    { id:1, from:"bot", text:lbl(
      `مرحباً بك في ${shopName}! 👋\nأنا مساعد الحجز الذكي.\nاكتب ما تريد مثل:\n"أريد حجز قص شعر بكرة الساعة 5"`,
      `Welcome to ${shopName}! 👋\nI'm your AI booking assistant.\nType something like:\n"I want a haircut tomorrow at 5pm"`
    ), ts:"الآن" }
  ]);
  const [input,setInput]=useState("");
  const [loading,setLoading]=useState(false);
  const [waConnected,setWaConnected]=useState(true);
  const endRef=useRef(null);

  useEffect(()=>{ endRef.current?.scrollIntoView({ behavior:"smooth" }); },[msgs]);

  const extractBooking=(text)=>{
    const svcMap={ "قص شعر":1, "تشذيب لحية":2, "صباغة شعر":3, "حلاقة":4, "عناية وجه":5, "أطفال":6,
                   "haircut":1, "beard":2, "color":3, "shave":4, "facial":5, "kids":6 };
    const foundSvcId=Object.entries(svcMap).find(([k])=>text.toLowerCase().includes(k.toLowerCase()))?.[1];
    const svc=services.find(s=>s.id===foundSvcId)||services[0];
    const timeMatch=text.match(/(\d{1,2})(?::(\d{2}))?\s*(pm|am|مساء|صباح|ً|ا)?/i);
    let extractedTime="10:00";
    if(timeMatch){
      let h=parseInt(timeMatch[1]);
      const isPm=timeMatch[3]&&(timeMatch[3].toLowerCase()==="pm"||timeMatch[3]==="مساء");
      if(isPm&&h<12) h+=12;
      extractedTime=`${String(h).padStart(2,"0")}:${timeMatch[2]||"00"}`;
    }
    const tomorrow=new Date(); tomorrow.setDate(tomorrow.getDate()+1);
    const dateStr=tomorrow.toISOString().split("T")[0];
    return { svc, time:extractedTime, date:dateStr };
  };

  const sendMsg=async()=>{
    if(!input.trim()||loading) return;
    const userText=input.trim();
    setInput("");
    const userMsg={ id:Date.now(), from:"user", text:userText, ts:"الآن" };
    setMsgs(p=>[...p,userMsg]);
    setLoading(true);

    await new Promise(r=>setTimeout(r,1400));

    const { svc, time, date }=extractBooking(userText);
    const barb=barbers[0];
    const dateObj=new Date(date);
    const dayNames=isRtl?["الأحد","الاثنين","الثلاثاء","الأربعاء","الخميس","الجمعة","السبت"]:["Sun","Mon","Tue","Wed","Thu","Fri","Sat"];
    const dayName=dayNames[dateObj.getDay()];

    const botReply=lbl(
      `✅ تم استلام طلبك!\n\n✂️ الخدمة: ${svc.nameAr}\n📅 الموعد: ${dayName}، ${date} الساعة ${time}\n💈 الحلاق: ${barb.name}\n💰 السعر: ${iqd(svc.price)}\n\nهل تريد تأكيد الحجز؟ اكتب *نعم* للتأكيد أو *لا* للإلغاء`,
      `✅ Request received!\n\n✂️ Service: ${svc.name}\n📅 Date: ${dayName}, ${date} at ${time}\n💈 Barber: ${barb.nameEn}\n💰 Price: ${iqd(svc.price)}\n\nReply *yes* to confirm or *no* to cancel`
    );

    setMsgs(p=>[...p,{ id:Date.now()+1, from:"bot", text:botReply, ts:"الآن",
      pendingBooking:{ customerId:1, barberId:barb.id, service:svc.nameAr,
        time, duration:svc.duration, status:"pending",
        payment:"cash", price:svc.price, note:"حجز عبر واتساب", source:"whatsapp" } }]);
    setLoading(false);
  };

  const handleConfirm=(msg)=>{
    if(msg.pendingBooking){
      onBookingCreated({ ...msg.pendingBooking, id:Date.now() });
      setMsgs(p=>[...p,
        { id:Date.now(), from:"user", text:lbl("نعم","yes"), ts:"الآن" },
        { id:Date.now()+1, from:"bot", ts:"الآن",
          text:lbl("🎉 تم تأكيد حجزك بنجاح!\nستصلك رسالة تذكير قبل موعدك بساعة.\nشكراً لاختيارك صالوننا 💈",
                   "🎉 Your booking is confirmed!\nYou'll receive a reminder 1 hour before.\nThank you for choosing us! 💈") }
      ]);
    }
  };

  return (
    <div style={{ position:"fixed", inset:0, zIndex:4000,
      fontFamily:"'Inter',-apple-system,sans-serif", direction:isRtl?"rtl":"ltr",
      display:"flex", flexDirection:"column" }}>
      {/* WhatsApp style bg */}
      <div style={{ position:"absolute", inset:0, background:"#0D1117",
        backgroundImage:"radial-gradient(circle at 20% 80%, #0B2217 0%, transparent 50%),radial-gradient(circle at 80% 20%, #0A1628 0%, transparent 50%)" }}/>

      {/* Header — WhatsApp style */}
      <div style={{ background:"#128C7E", padding:"12px 16px", display:"flex",
        alignItems:"center", gap:12, position:"relative", zIndex:10,
        boxShadow:"0 2px 8px #00000055" }}>
        <button onClick={onClose} style={{ background:"none", border:"none",
          cursor:"pointer", color:"#fff", padding:4 }}>
          <I n="x" s={20} c="#fff"/>
        </button>
        <div style={{ width:40, height:40, borderRadius:"50%", background:"#075E54",
          display:"flex", alignItems:"center", justifyContent:"center" }}>
          <I n="scissors" s={20} c="#fff"/>
        </div>
        <div style={{ flex:1 }}>
          <div style={{ fontWeight:700, color:"#fff", fontSize:16 }}>{shopName}</div>
          <div style={{ color:"#d0ebe7", fontSize:12, display:"flex", alignItems:"center", gap:5 }}>
            <div style={{ width:8, height:8, borderRadius:"50%", background:"#25D366" }}/>
            {lbl("متصل — مساعد ذكاء اصطناعي","Online — AI Assistant")}
          </div>
        </div>
        <div style={{ background:"#075E54", borderRadius:8, padding:"4px 10px",
          color:"#25D366", fontSize:11, fontWeight:700 }}>
          🤖 AI
        </div>
      </div>

      {/* Messages area */}
      <div style={{ flex:1, overflowY:"auto", padding:"16px 12px",
        position:"relative", zIndex:1 }}>
        {msgs.map(m=>(
          <div key={m.id} style={{ display:"flex",
            justifyContent:m.from==="user"?"flex-end":"flex-start",
            marginBottom:10 }}>
            <div style={{ maxWidth:"82%",
              background:m.from==="user"?"#005C4B":"#1F2C34",
              borderRadius:m.from==="user"?"16px 4px 16px 16px":"4px 16px 16px 16px",
              padding:"10px 14px",
              boxShadow:"0 1px 3px #00000055" }}>
              <div style={{ color:"#E9EDEF", fontSize:14, lineHeight:1.6,
                whiteSpace:"pre-line" }}>{m.text}</div>
              <div style={{ color:"#8696A0", fontSize:10, marginTop:4,
                textAlign:m.from==="user"?"right":"left" }}>{m.ts}</div>
              {m.pendingBooking&&(
                <div style={{ marginTop:10, display:"flex", gap:8 }}>
                  <button onClick={()=>handleConfirm(m)}
                    style={{ flex:1, background:"#25D366", border:"none", borderRadius:8,
                      padding:"8px", color:"#fff", fontWeight:700, cursor:"pointer",
                      fontSize:13, fontFamily:"inherit" }}>
                    {lbl("✓ نعم، أؤكد","✓ Yes, confirm")}
                  </button>
                  <button onClick={()=>setMsgs(p=>[...p,
                    { id:Date.now(), from:"user", text:lbl("لا","no"), ts:"الآن" },
                    { id:Date.now()+1, from:"bot", text:lbl("حسناً، تم الإلغاء. يمكنك الحجز في أي وقت 😊","Okay, cancelled. You can book anytime 😊"), ts:"الآن" }
                  ])}
                    style={{ flex:1, background:"#FF4757", border:"none", borderRadius:8,
                      padding:"8px", color:"#fff", fontWeight:700, cursor:"pointer",
                      fontSize:13, fontFamily:"inherit" }}>
                    {lbl("✗ لا","✗ No")}
                  </button>
                </div>
              )}
            </div>
          </div>
        ))}
        {loading&&(
          <div style={{ display:"flex", justifyContent:"flex-start", marginBottom:10 }}>
            <div style={{ background:"#1F2C34", borderRadius:"4px 16px 16px 16px",
              padding:"12px 16px" }}>
              <div style={{ display:"flex", gap:5, alignItems:"center" }}>
                {[0,1,2].map(i=>(
                  <div key={i} style={{ width:8, height:8, borderRadius:"50%",
                    background:"#8696A0", animation:`bounce .8s ${i*0.2}s infinite alternate` }}/>
                ))}
              </div>
            </div>
          </div>
        )}
        <div ref={endRef}/>
      </div>

      {/* Input */}
      <div style={{ background:"#1F2C34", padding:"10px 12px",
        display:"flex", gap:10, alignItems:"center", position:"relative", zIndex:10 }}>
        <input value={input} onChange={e=>setInput(e.target.value)}
          onKeyDown={e=>e.key==="Enter"&&sendMsg()}
          placeholder={lbl("اكتب رسالتك…","Type a message…")}
          style={{ flex:1, background:"#2A3942", border:"none", borderRadius:22,
            padding:"11px 16px", color:"#E9EDEF", fontSize:14, outline:"none",
            fontFamily:"inherit" }}/>
        <button onClick={sendMsg} disabled={!input.trim()||loading}
          style={{ width:44, height:44, borderRadius:"50%", background:"#128C7E",
            border:"none", cursor:input.trim()?"pointer":"default",
            display:"flex", alignItems:"center", justifyContent:"center",
            opacity:input.trim()?1:0.5, transition:"opacity .2s" }}>
          <I n="trend" s={18} c="#fff"/>
        </button>
      </div>

      <style>{`
        @keyframes bounce{ from{transform:translateY(0)}to{transform:translateY(-4px)} }
      `}</style>
    </div>
  );
};


const DashboardPage = ({ t, lang, appts, customers, services, barbers, onAction, onNewBooking }) => {
  const done=appts.filter(a=>a.status==="confirmed"||a.status==="completed");
  const rev=done.reduce((s,a)=>s+a.price,0);
  const pending=appts.filter(a=>a.status==="pending");
  const days=lang==="ar"?DAYS_AR:DAYS_EN;
  const cancelR=appts.length?Math.round((appts.filter(a=>a.status==="cancelled").length/appts.length)*100):0;
  const topSvc=(()=>{ const m={}; done.forEach(a=>{ m[a.service]=(m[a.service]||0)+1; });
    return Object.entries(m).sort((a,b)=>b[1]-a[1])[0]?.[0]||"—"; })();
  const waMsgs=appts.filter(a=>a.source==="whatsapp").length;
  return (
    <div>
      <div style={{ marginBottom:18 }}>
        <div style={{ fontSize:22, fontWeight:900, color:C.text, letterSpacing:"-0.02em" }}>
          {t.dash.greeting}, <span style={{ color:C.gold }}>Omar 👋</span>
        </div>
        <div style={{ color:C.textSec, fontSize:13, marginTop:4 }}>
          {lang==="ar"?"مواعيد اليوم":"Today's schedule"}: <b style={{ color:C.text }}>{done.length}</b> {t.dash.appts}
        </div>
      </div>
      <div style={{ display:"grid", gridTemplateColumns:"1fr 1fr", gap:10, marginBottom:16 }}>
        <StatCard icon="dollar" label={t.dash.revenue} value={iqd(rev)} wide
          sub={lang==="ar"?"+12% مقارنة بالأمس":"+12% vs yesterday"} color={C.gold}/>
        <StatCard icon="calendar" label={t.dash.appts} value={appts.length}
          sub={`${done.length} ${t.status.confirmed}`} color={C.blue}/>
        <StatCard icon="users" label={t.dash.customers} value={customers.length}
          sub={`3 ${lang==="ar"?"جدد":"new"}`} color={C.purple}/>
      </div>
      <div style={{ display:"grid", gridTemplateColumns:"repeat(3,1fr)", gap:8, marginBottom:16 }}>
        {[[t.dash.cancelRate,`${cancelR}%`,C.red],[t.dash.popularService,topSvc,C.gold],[t.dash.waMessages,waMsgs,C.green]].map(([l,v,c],i)=>(
          <div key={i} style={{ background:C.surface, border:`1px solid ${C.border}`,
            borderRadius:13, padding:"12px 10px", textAlign:"center" }}>
            <div style={{ color:c, fontWeight:900, fontSize:14, marginBottom:3 }}>{v}</div>
            <div style={{ color:C.textMuted, fontSize:10, fontWeight:600 }}>{l}</div>
          </div>
        ))}
      </div>
      <Card style={{ marginBottom:14 }}>
        <div style={{ display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:12 }}>
          <div style={{ fontWeight:800, color:C.text, fontSize:14 }}>{t.dash.weeklyRevenue}</div>
          <div style={{ fontWeight:900, color:C.gold, fontSize:15 }}>{iqd(2960000)}</div>
        </div>
        <BarChart data={WEEKLY_REV} labels={days} hl={new Date().getDay()}/>
      </Card>
      {pending.length>0&&(
        <div style={{ marginBottom:14 }}>
          <div style={{ display:"flex", alignItems:"center", gap:8, marginBottom:10 }}>
            <div style={{ width:8, height:8, borderRadius:"50%", background:C.gold,
              boxShadow:`0 0 6px ${C.gold}`, flexShrink:0 }}/>
            <div style={{ fontWeight:700, color:C.text }}>{t.dash.pendingLabel}</div>
            <span style={{ background:C.goldFaint, color:C.gold, padding:"2px 8px",
              borderRadius:10, fontSize:11, fontWeight:800 }}>{pending.length}</span>
          </div>
          <div style={{ display:"flex", flexDirection:"column", gap:8 }}>
            {pending.map(a=><ApptRow key={a.id} appt={a} customers={customers} barbers={barbers}
              t={t} onAccept={id=>onAction("accept",id)} onReject={id=>onAction("reject",id)}/>)}
          </div>
        </div>
      )}
      <Card>
        <div style={{ display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:12 }}>
          <div style={{ fontWeight:700, color:C.text }}>{t.dash.upcomingLabel}</div>
          <Btn onClick={onNewBooking} style={{ padding:"7px 13px", fontSize:12 }}>+ {t.book.newBooking}</Btn>
        </div>
        {done.length===0
          ? <EmptyState icon="calendar" title={t.book.noAppts} sub={t.book.bookFirst}/>
          : <div style={{ display:"flex", flexDirection:"column", gap:8 }}>
              {done.slice(0,4).map(a=><ApptRow key={a.id} appt={a} customers={customers}
                barbers={barbers} t={t} onAccept={()=>{}} onReject={()=>{}}/>)}
            </div>}
      </Card>
    </div>
  );
};

const BookingsPage = ({ t, appts, setAppts, customers, services, barbers, showToast }) => {
  const [filter,setFilter]=useState("all"); const [open,setOpen]=useState(false);
  const depSet={ type:"none", value:0 };
  const shown=filter==="all"?appts:appts.filter(a=>a.status===filter);
  const handle=(action,id)=>{ setAppts(p=>p.map(a=>a.id===id?{...a,status:action==="accept"?"confirmed":"cancelled"}:a));
    showToast(action==="accept"?(t.dir==="rtl"?"✓ تم القبول":"✓ Confirmed"):(t.dir==="rtl"?"تم الرفض":"Rejected"),action==="accept"?"success":"error"); };
  return (
    <div>
      <div style={{ display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:16 }}>
        <div style={{ fontSize:20, fontWeight:900, color:C.text }}>{t.book.title}</div>
        <Btn onClick={()=>setOpen(true)} style={{ padding:"8px 13px", fontSize:13,
          display:"flex", alignItems:"center", gap:6 }}>
          <I n="plus" s={14} c={C.bg}/>{t.book.newBooking}
        </Btn>
      </div>
      <div style={{ display:"flex", gap:6, marginBottom:16, overflowX:"auto", paddingBottom:4 }}>
        {["all","confirmed","pending","completed","cancelled"].map(k=>(
          <Pill key={k} active={filter===k} onClick={()=>setFilter(k)}>{t.book[`filter_${k}`]}</Pill>
        ))}
      </div>
      {shown.length===0
        ? <EmptyState icon="calendar" title={t.book.noAppts} sub={t.book.bookFirst}
            action={<Btn onClick={()=>setOpen(true)}>+ {t.book.newBooking}</Btn>}/>
        : <div style={{ display:"flex", flexDirection:"column", gap:8 }}>
            {shown.map(a=><ApptRow key={a.id} appt={a} customers={customers} barbers={barbers} t={t}
              onAccept={id=>handle("accept",id)} onReject={id=>handle("reject",id)}/>)}
          </div>}
      <BookingModal open={open} onClose={()=>setOpen(false)} customers={customers}
        services={services} barbers={barbers} t={t} depSet={depSet}
        onSave={a=>{ setAppts(p=>[...p,a]); showToast(t.dir==="rtl"?"✓ تم إنشاء الحجز":"✓ Booking created"); }}/>
    </div>
  );
};

const CustomersPage = ({ t, customers, setCustomers, appts, showToast }) => {
  const [search,setSearch]=useState("");
  const [open,setOpen]=useState(false);
  const [confirmDel,setConfirmDel]=useState(null);
  const [editTarget,setEditTarget]=useState(null);
  const [form,setForm]=useState({ name:"", nameAr:"", phone:"", notes:"" });
  const isRtl=t.dir==="rtl";

  const filtered=customers.filter(c=>(c.name+c.nameAr+c.phone).toLowerCase().includes(search.toLowerCase()));
  const spent=id=>appts.filter(a=>a.customerId===id&&(a.status==="confirmed"||a.status==="completed")).reduce((s,a)=>s+a.price,0)||(customers.find(c=>c.id===id)?.spent||0);

  const openAdd=()=>{ setForm({name:"",nameAr:"",phone:"",notes:""}); setEditTarget(null); setOpen(true); };
  const openEdit=c=>{ setForm({name:c.name,nameAr:c.nameAr,phone:c.phone,notes:c.notes||""}); setEditTarget(c.id); setOpen(true); };

  const handleSave=()=>{
    if(!form.name.trim()) return;
    if(editTarget){
      setCustomers(p=>p.map(c=>c.id===editTarget?{...c,...form,avatar:(form.nameAr||form.name)[0]}:c));
      showToast(isRtl?"✓ تم تحديث بيانات العميل":"✓ Customer updated");
    } else {
      setCustomers(p=>[...p,{ id:Date.now(), name:form.name, nameAr:form.nameAr||form.name,
        phone:form.phone, visits:0, spent:0, lastVisit:"—", loyal:false,
        avatar:(form.nameAr||form.name)[0], favService:"—", notes:form.notes }]);
      showToast(isRtl?"✓ تم إضافة العميل":"✓ Customer added");
    }
    setForm({name:"",nameAr:"",phone:"",notes:""}); setOpen(false); setEditTarget(null);
  };

  const handleDelete=id=>{
    setCustomers(p=>p.filter(c=>c.id!==id));
    showToast(isRtl?"تم حذف العميل":"Customer deleted","error");
    setConfirmDel(null);
  };

  return (
    <div>
      <div style={{ display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:16 }}>
        <div style={{ fontSize:20, fontWeight:900, color:C.text }}>{t.customers.title}</div>
        <Btn onClick={openAdd} style={{ padding:"8px 13px", fontSize:13,
          display:"flex", alignItems:"center", gap:6 }}>
          <I n="plus" s={14} c={C.bg}/>{t.customers.addCustomer}
        </Btn>
      </div>
      <div style={{ position:"relative", marginBottom:14 }}>
        <div style={{ position:"absolute", left:13, top:"50%", transform:"translateY(-50%)" }}>
          <I n="search" s={16} c={C.textMuted}/>
        </div>
        <input value={search} onChange={e=>setSearch(e.target.value)} placeholder={t.customers.search}
          style={{ width:"100%", background:C.surface, border:`1px solid ${C.border}`,
            borderRadius:12, padding:"11px 12px 11px 42px", color:C.text,
            fontSize:14, outline:"none", boxSizing:"border-box", fontFamily:"inherit" }}/>
      </div>
      {filtered.length===0
        ? <EmptyState icon="users" title={t.customers.noResults}
            action={<Btn onClick={openAdd}>+ {t.customers.addCustomer}</Btn>}/>
        : <div style={{ display:"flex", flexDirection:"column", gap:10 }}>
            {filtered.map(c=>{
              const sp=spent(c.id);
              const vs=appts.filter(a=>a.customerId===c.id).length||c.visits;
              return (
                <Card key={c.id}>
                  <div style={{ display:"flex", alignItems:"center", gap:12, marginBottom:12 }}>
                    <Av char={c.avatar} size={46} bg={c.loyal?C.gold:C.textMuted}/>
                    <div style={{ flex:1 }}>
                      <div style={{ display:"flex", alignItems:"center", gap:7, flexWrap:"wrap" }}>
                        <span style={{ fontWeight:800, color:C.text }}>{isRtl?c.nameAr:c.name}</span>
                        {c.loyal&&<span style={{ fontSize:10, background:C.goldFaint, color:C.gold,
                          padding:"2px 8px", borderRadius:10, fontWeight:700,
                          display:"flex", alignItems:"center", gap:3 }}>
                          <I n="star" s={9} c={C.gold}/>{t.customers.loyal}
                        </span>}
                      </div>
                      <div style={{ color:C.textSec, fontSize:12, marginTop:3,
                        display:"flex", alignItems:"center", gap:4 }}>
                        <I n="phone" s={11} c={C.textMuted}/>{c.phone}
                      </div>
                      {c.favService&&c.favService!=="—"&&(
                        <div style={{ color:C.textMuted, fontSize:11, marginTop:3 }}>✂️ {c.favService}</div>
                      )}
                    </div>
                    {/* أزرار التحكم */}
                    <div style={{ display:"flex", gap:6 }}>
                      <button onClick={()=>openEdit(c)}
                        style={{ width:32, height:32, borderRadius:9, background:C.surfaceHigh,
                          border:"none", cursor:"pointer",
                          display:"flex", alignItems:"center", justifyContent:"center" }}>
                        <I n="edit" s={14} c={C.textSec}/>
                      </button>
                      <button onClick={()=>setConfirmDel(c)}
                        style={{ width:32, height:32, borderRadius:9, background:C.redFaint,
                          border:`1px solid ${C.red}33`, cursor:"pointer",
                          display:"flex", alignItems:"center", justifyContent:"center" }}>
                        <I n="trash" s={14} c={C.red}/>
                      </button>
                    </div>
                  </div>
                  <div style={{ display:"flex", borderTop:`1px solid ${C.border}`, paddingTop:12 }}>
                    {[[t.customers.totalVisits,vs],[t.customers.totalSpent,iqd(sp)],[t.customers.lastVisit,c.lastVisit]].map(([l,v],i)=>(
                      <div key={i} style={{ flex:1, textAlign:i===0?"left":i===1?"center":"right" }}>
                        <div style={{ color:C.textMuted, fontSize:10, marginBottom:3, fontWeight:600 }}>{l}</div>
                        <div style={{ color:C.text, fontWeight:800, fontSize:14 }}>{v}</div>
                      </div>
                    ))}
                  </div>
                  {c.notes&&<div style={{ marginTop:10, padding:"8px 12px",
                    background:C.surfaceMid, borderRadius:8, color:C.textSec, fontSize:12 }}>
                    📝 {c.notes}
                  </div>}
                </Card>
              );
            })}
          </div>}

      {/* Modal تأكيد الحذف */}
      {confirmDel&&(
        <div onClick={()=>setConfirmDel(null)}
          style={{ position:"fixed", inset:0, background:"#000c", zIndex:2000,
            display:"flex", alignItems:"center", justifyContent:"center", padding:20 }}>
          <div onClick={e=>e.stopPropagation()}
            style={{ background:C.surface, border:`1px solid ${C.red}44`,
              borderRadius:20, padding:28, maxWidth:340, width:"100%", textAlign:"center" }}>
            <div style={{ width:60, height:60, borderRadius:18, background:C.redFaint,
              display:"flex", alignItems:"center", justifyContent:"center", margin:"0 auto 16px" }}>
              <I n="trash" s={28} c={C.red}/>
            </div>
            <div style={{ fontWeight:800, color:C.text, fontSize:18, marginBottom:8 }}>
              {isRtl?"حذف العميل؟":"Delete Customer?"}
            </div>
            <div style={{ color:C.textSec, fontSize:14, marginBottom:6 }}>
              <b style={{ color:C.text }}>{isRtl?confirmDel.nameAr:confirmDel.name}</b>
            </div>
            <div style={{ color:C.textMuted, fontSize:13, marginBottom:24, lineHeight:1.5 }}>
              {isRtl
                ?"سيتم حذف بيانات العميل نهائياً ولا يمكن التراجع"
                :"This will permanently delete the customer. Cannot be undone."}
            </div>
            <div style={{ display:"flex", gap:10 }}>
              <Btn onClick={()=>setConfirmDel(null)} v="ghost" style={{ flex:1 }}>
                {isRtl?"إلغاء":"Cancel"}
              </Btn>
              <Btn onClick={()=>handleDelete(confirmDel.id)} v="danger" style={{ flex:1 }}>
                {isRtl?"حذف نهائي":"Delete"}
              </Btn>
            </div>
          </div>
        </div>
      )}
      <Modal open={open} onClose={()=>{ setOpen(false); setEditTarget(null); }}
        title={editTarget
          ? (isRtl?"تعديل بيانات العميل":"Edit Customer")
          : t.customers.addCustomer}>
        <Inp label="Name (EN)" value={form.name} onChange={v=>setForm(p=>({...p,name:v}))} placeholder="Ali Ahmed"/>
        <Inp label="الاسم (AR)" value={form.nameAr} onChange={v=>setForm(p=>({...p,nameAr:v}))} placeholder="علي أحمد"/>
        <Inp label={t.customers.phone} value={form.phone} onChange={v=>setForm(p=>({...p,phone:v}))} type="tel" placeholder="07XX XXX XXXX"/>
        <Inp label={t.customers.notes} value={form.notes} onChange={v=>setForm(p=>({...p,notes:v}))} placeholder="…"/>
        <div style={{ display:"flex", gap:10 }}>
          <Btn onClick={()=>{ setOpen(false); setEditTarget(null); }} v="ghost" style={{ flex:1 }}>
            {isRtl?"إلغاء":"Cancel"}
          </Btn>
          <Btn onClick={handleSave} disabled={!form.name.trim()} style={{ flex:2 }}>
            {editTarget?(isRtl?"حفظ التعديلات":"Save Changes"):t.customers.addCustomer}
          </Btn>
        </div>
      </Modal>
    </div>
  );
};

const ServicesPage = ({ t, services, setServices, showToast }) => {
  const [open,setOpen]=useState(false); const [editId,setEditId]=useState(null);
  const [form,setForm]=useState({ name:"", nameAr:"", duration:30, price:0, color:C.gold });
  const PAL=[C.gold,C.amber,C.blue,C.green,C.purple,C.red];
  const openAdd=()=>{ setForm({name:"",nameAr:"",duration:30,price:0,color:C.gold});setEditId(null);setOpen(true); };
  const openEdit=s=>{ setForm({...s});setEditId(s.id);setOpen(true); };
  const save=()=>{ if(!form.name.trim()) return;
    if(editId){ setServices(p=>p.map(s=>s.id===editId?{...form,id:editId}:s));
      showToast(t.dir==="rtl"?"✓ تم التحديث":"✓ Updated"); }
    else { setServices(p=>[...p,{...form,id:Date.now()}]);
      showToast(t.dir==="rtl"?"✓ تمت الإضافة":"✓ Added"); }
    setOpen(false); };
  return (
    <div>
      <div style={{ display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:16 }}>
        <div style={{ fontSize:20, fontWeight:900, color:C.text }}>{t.services.title}</div>
        <Btn onClick={openAdd} style={{ padding:"8px 13px", fontSize:13,
          display:"flex", alignItems:"center", gap:6 }}>
          <I n="plus" s={14} c={C.bg}/>{t.services.addService}
        </Btn>
      </div>
      {services.length===0
        ? <EmptyState icon="scissors" title={t.services.noServices} sub={t.services.addFirst}
            action={<Btn onClick={openAdd}>+ {t.services.addService}</Btn>}/>
        : <div style={{ display:"flex", flexDirection:"column", gap:10 }}>
            {services.map(s=>(
              <Card key={s.id} style={{ display:"flex", alignItems:"center", gap:14 }}>
                <div style={{ width:46, height:46, borderRadius:13, background:`${s.color}18`,
                  display:"flex", alignItems:"center", justifyContent:"center", flexShrink:0 }}>
                  <I n="scissors" s={20} c={s.color}/>
                </div>
                <div style={{ flex:1 }}>
                  <div style={{ fontWeight:800, color:C.text, fontSize:15 }}>{t.dir==="rtl"?s.nameAr:s.name}</div>
                  <div style={{ color:C.textSec, fontSize:12, marginTop:3, display:"flex", alignItems:"center", gap:3 }}>
                    <I n="clock" s={11} c={C.textMuted}/>{s.duration} {t.mins}
                  </div>
                </div>
                <div style={{ fontWeight:900, color:s.color, fontSize:16 }}>{iqd(s.price)}</div>
                <div style={{ display:"flex", gap:6 }}>
                  <button onClick={()=>openEdit(s)} style={{ width:32, height:32, borderRadius:9,
                    background:C.surfaceHigh, border:"none", cursor:"pointer",
                    display:"flex", alignItems:"center", justifyContent:"center" }}>
                    <I n="edit" s={14} c={C.textSec}/>
                  </button>
                  <button onClick={()=>{ setServices(p=>p.filter(x=>x.id!==s.id));
                    showToast(t.dir==="rtl"?"تم الحذف":"Deleted","error"); }}
                    style={{ width:32, height:32, borderRadius:9, background:C.redFaint,
                      border:"none", cursor:"pointer",
                      display:"flex", alignItems:"center", justifyContent:"center" }}>
                    <I n="trash" s={14} c={C.red}/>
                  </button>
                </div>
              </Card>
            ))}
          </div>}
      <Modal open={open} onClose={()=>setOpen(false)} title={editId?t.services.edit:t.services.addService}>
        <Inp label={t.services.name_en} value={form.name} onChange={v=>setForm(p=>({...p,name:v}))} placeholder="Haircut"/>
        <Inp label={t.services.name_ar} value={form.nameAr} onChange={v=>setForm(p=>({...p,nameAr:v}))} placeholder="قص شعر"/>
        <div style={{ display:"flex", gap:12 }}>
          <div style={{ flex:1 }}><Inp label={t.services.duration} value={String(form.duration)}
            onChange={v=>setForm(p=>({...p,duration:Number(v)}))} type="number"/></div>
          <div style={{ flex:1 }}><Inp label={`${t.services.price} (د.ع)`} value={String(form.price)}
            onChange={v=>setForm(p=>({...p,price:Number(v)}))} type="number"/></div>
        </div>
        <div style={{ marginBottom:18 }}>
          <div style={{ color:C.textSec, fontSize:12, marginBottom:8, fontWeight:600 }}>Color</div>
          <div style={{ display:"flex", gap:10 }}>
            {PAL.map(col=>(
              <div key={col} onClick={()=>setForm(p=>({...p,color:col}))}
                style={{ width:32, height:32, borderRadius:"50%", background:col, cursor:"pointer",
                  border:`3px solid ${form.color===col?C.text:"transparent"}`, transition:"border .15s" }}/>
            ))}
          </div>
        </div>
        <div style={{ display:"flex", gap:10 }}>
          <Btn onClick={()=>setOpen(false)} v="ghost" style={{ flex:1 }}>{t.services.cancel}</Btn>
          <Btn onClick={save} disabled={!form.name.trim()} style={{ flex:2 }}>{t.services.save}</Btn>
        </div>
      </Modal>
    </div>
  );
};
const FinancePage = ({ t, lang, appts }) => {
  const [period,setPeriod]=useState("today");
  const days=lang==="ar"?DAYS_AR:DAYS_EN;
  const done=appts.filter(a=>a.status==="confirmed"||a.status==="completed");
  const rev=done.reduce((s,a)=>s+a.price,0);
  const cashR=done.filter(a=>a.payment==="cash").reduce((s,a)=>s+a.price,0);
  const onlineR=done.filter(a=>a.payment==="online").reduce((s,a)=>s+a.price,0);
  const depR=done.filter(a=>a.payment==="deposit").reduce((s,a)=>s+a.price,0);
  const pct=v=>rev>0?Math.round((v/rev)*100):0;
  const cancelR=appts.length?Math.round((appts.filter(a=>a.status==="cancelled").length/appts.length)*100):0;
  return (
    <div>
      <div style={{ fontSize:20, fontWeight:900, color:C.text, marginBottom:16 }}>{t.finance.title}</div>
      <div style={{ display:"flex", gap:8, marginBottom:16 }}>
        {[["today",t.finance.today],["week",t.finance.week],["month",t.finance.month]].map(([k,l])=>(
          <button key={k} onClick={()=>setPeriod(k)} style={{ flex:1, padding:"10px", borderRadius:11,
            border:`1px solid ${period===k?C.gold:C.border}`, fontFamily:"inherit",
            background:period===k?C.gold:C.surface, color:period===k?C.bg:C.textSec,
            fontWeight:800, fontSize:13, cursor:"pointer", transition:"all .15s" }}>{l}</button>
        ))}
      </div>
      <div style={{ background:`linear-gradient(135deg,${C.goldFaint},${C.surface})`,
        border:`1px solid ${C.gold}33`, borderRadius:20, padding:"22px 18px",
        marginBottom:14, textAlign:"center", position:"relative", overflow:"hidden" }}>
        <div style={{ position:"absolute", top:-20, right:-20, width:100, height:100,
          borderRadius:"50%", background:`${C.gold}08` }}/>
        <div style={{ color:C.textSec, fontSize:13, marginBottom:6 }}>{t.finance.totalRevenue}</div>
        <div style={{ fontSize:40, fontWeight:900, color:C.gold, letterSpacing:"-0.03em", lineHeight:1 }}>
          {rev.toLocaleString("ar-IQ")}
        </div>
        <div style={{ color:C.textSec, fontSize:15, marginTop:4 }}>د.ع</div>
        <div style={{ display:"flex", justifyContent:"center", gap:22, marginTop:16,
          paddingTop:16, borderTop:`1px solid ${C.gold}22` }}>
          {[[t.finance.dailyAvg,iqd(Math.round(rev/7))],[t.finance.busiest,lang==="ar"?"الخميس":"Thursday"],[t.dash.appts,done.length]].map(([k,v],i)=>(
            <div key={i}>
              <div style={{ color:C.textMuted, fontSize:10, fontWeight:600 }}>{k}</div>
              <div style={{ color:C.text, fontWeight:800, fontSize:13, marginTop:2 }}>{v}</div>
            </div>
          ))}
        </div>
      </div>
      <div style={{ display:"grid", gridTemplateColumns:"1fr 1fr", gap:10, marginBottom:14 }}>
        <Card style={{ textAlign:"center" }}>
          <SparkPie value={cancelR} color={C.red}/>
          <div style={{ color:C.textMuted, fontSize:11, marginTop:6, fontWeight:600 }}>{t.finance.cancelRate}</div>
        </Card>
        <Card style={{ textAlign:"center" }}>
          <SparkPie value={68} color={C.green}/>
          <div style={{ color:C.textMuted, fontSize:11, marginTop:6, fontWeight:600 }}>{t.finance.returnRate}</div>
        </Card>
      </div>
      <Card style={{ marginBottom:14 }}>
        <div style={{ fontWeight:700, color:C.text, marginBottom:12 }}>{t.finance.peakHour}</div>
        <BarChart data={PEAK_HOURS} labels={PEAK_LBL} hl={4}/>
      </Card>
      <Card style={{ marginBottom:14 }}>
        <div style={{ fontWeight:700, color:C.text, marginBottom:12 }}>
          {lang==="ar"?"الإيرادات اليومية":"Daily Revenue"}
        </div>
        <BarChart data={WEEKLY_REV} labels={days} hl={new Date().getDay()}/>
      </Card>
      <Card style={{ marginBottom:14 }}>
        <div style={{ fontWeight:700, color:C.text, marginBottom:12 }}>
          {lang==="ar"?"طرق الدفع":"Payment Methods"}
        </div>
        {[[t.finance.cash,cashR,C.gold],[t.finance.online,onlineR,C.blue],[t.finance.deposit,depR,C.amber]].map(([l,v,col])=>(
          <div key={l} style={{ marginBottom:14 }}>
            <div style={{ display:"flex", justifyContent:"space-between", marginBottom:6 }}>
              <span style={{ color:C.textSec, fontSize:13, display:"flex", alignItems:"center", gap:6 }}>
                <div style={{ width:8, height:8, borderRadius:"50%", background:col }}/>{l}
              </span>
              <div style={{ display:"flex", gap:8 }}>
                <span style={{ color:C.textMuted, fontSize:12 }}>{iqd(v)}</span>
                <span style={{ color:col, fontWeight:700, fontSize:13 }}>{pct(v)}%</span>
              </div>
            </div>
            <div style={{ height:7, borderRadius:4, background:C.surfaceHigh }}>
              <div style={{ width:`${pct(v)}%`, height:"100%", borderRadius:4,
                background:col, transition:"width .9s ease" }}/>
            </div>
          </div>
        ))}
      </Card>
      <Card>
        <div style={{ fontWeight:700, color:C.text, marginBottom:12 }}>{t.finance.transactions}</div>
        {done.length===0
          ? <div style={{ textAlign:"center", color:C.textMuted, padding:20 }}>—</div>
          : done.map(a=>{ const pc=a.payment==="cash"?C.gold:a.payment==="online"?C.blue:C.amber;
              const pl=a.payment==="cash"?t.finance.cash:a.payment==="online"?t.finance.online:t.finance.deposit;
              return (
                <div key={a.id} style={{ display:"flex", alignItems:"center", gap:10,
                  padding:"10px 0", borderBottom:`1px solid ${C.border}` }}>
                  <div style={{ width:34, height:34, borderRadius:10, background:`${pc}18`,
                    display:"flex", alignItems:"center", justifyContent:"center", flexShrink:0 }}>
                    <I n="dollar" s={15} c={pc}/>
                  </div>
                  <div style={{ flex:1 }}>
                    <div style={{ color:C.text, fontSize:13, fontWeight:600 }}>{a.service}</div>
                    <div style={{ color:C.textMuted, fontSize:11, marginTop:2 }}>{a.time} · {pl}</div>
                  </div>
                  <div style={{ fontWeight:800, color:C.green, fontSize:13 }}>+{iqd(a.price)}</div>
                </div>
              );
            })}
      </Card>
    </div>
  );
};

const BarbersPage = ({ t, barbers, setBarbers, showToast }) => {
  const [open,setOpen]=useState(false);
  const [form,setForm]=useState({ name:"", nameEn:"", specialty:"" });
  const COLS=[C.gold,C.blue,C.green,C.purple,C.amber,C.red];
  return (
    <div>
      <div style={{ display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:16 }}>
        <div style={{ fontSize:20, fontWeight:900, color:C.text }}>{t.barbers.title}</div>
        <Btn onClick={()=>{ setForm({name:"",nameEn:"",specialty:""});setOpen(true); }}
          style={{ padding:"8px 13px", fontSize:13, display:"flex", alignItems:"center", gap:6 }}>
          <I n="plus" s={14} c={C.bg}/>{t.barbers.addBarber}
        </Btn>
      </div>
      {barbers.length===0
        ? <EmptyState icon="users" title={t.barbers.noBarbers}/>
        : <div style={{ display:"flex", flexDirection:"column", gap:10 }}>
            {barbers.map((b,i)=>(
              <Card key={b.id} style={{ display:"flex", alignItems:"center", gap:14 }}>
                <Av char={b.avatar} size={52} bg={COLS[i%COLS.length]}/>
                <div style={{ flex:1 }}>
                  <div style={{ fontWeight:800, color:C.text, fontSize:16 }}>
                    {t.dir==="rtl"?b.name:b.nameEn}
                  </div>
                  <div style={{ color:C.textSec, fontSize:13, marginTop:3 }}>✂️ {b.specialty}</div>
                  <div style={{ color:C.textMuted, fontSize:12, marginTop:3 }}>
                    📅 {b.bookings} {t.book.title}
                  </div>
                </div>
                <div style={{ display:"flex", gap:6 }}>
                  <button style={{ width:32, height:32, borderRadius:9, background:C.surfaceHigh,
                    border:"none", cursor:"pointer", display:"flex", alignItems:"center", justifyContent:"center" }}>
                    <I n="edit" s={14} c={C.textSec}/>
                  </button>
                  <button onClick={()=>{ setBarbers(p=>p.filter(x=>x.id!==b.id));
                    showToast(t.dir==="rtl"?"تم الحذف":"Deleted","error"); }}
                    style={{ width:32, height:32, borderRadius:9, background:C.redFaint,
                      border:"none", cursor:"pointer", display:"flex", alignItems:"center", justifyContent:"center" }}>
                    <I n="trash" s={14} c={C.red}/>
                  </button>
                </div>
              </Card>
            ))}
          </div>}
      <Modal open={open} onClose={()=>setOpen(false)} title={t.barbers.addBarber}>
        <Inp label={`${t.barbers.name} (AR)`} value={form.name}
          onChange={v=>setForm(p=>({...p,name:v,avatar:v[0]||""}))} placeholder="أبو علي"/>
        <Inp label={`${t.barbers.name} (EN)`} value={form.nameEn}
          onChange={v=>setForm(p=>({...p,nameEn:v}))} placeholder="Abu Ali"/>
        <Inp label={t.barbers.specialty} value={form.specialty}
          onChange={v=>setForm(p=>({...p,specialty:v}))} placeholder="قص وتشذيب"/>
        <div style={{ display:"flex", gap:10 }}>
          <Btn onClick={()=>setOpen(false)} v="ghost" style={{ flex:1 }}>{t.modal.cancel}</Btn>
          <Btn onClick={()=>{ if(!form.name.trim()) return;
            setBarbers(p=>[...p,{...form,id:Date.now(),bookings:0,color:C.gold}]);
            setOpen(false); showToast(t.dir==="rtl"?"✓ تمت الإضافة":"✓ Added"); }}
            disabled={!form.name.trim()} style={{ flex:2 }}>{t.save}</Btn>
        </div>
      </Modal>
    </div>
  );
};

const NotificationsPage = ({ t, lang, notifs, setNotifs }) => {
  const TYPE={ booking:{icon:"calendar",col:C.gold}, reminder:{icon:"bell",col:C.amber},
               payment:{icon:"dollar",col:C.green}, system:{icon:"trend",col:C.blue},
               whatsapp:{icon:"wa",col:"#25D366"} };
  const unread=notifs.filter(n=>!n.read).length;
  return (
    <div>
      <div style={{ display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:16 }}>
        <div style={{ display:"flex", alignItems:"center", gap:10 }}>
          <div style={{ fontSize:20, fontWeight:900, color:C.text }}>{t.notif.title}</div>
          {unread>0&&<span style={{ background:C.gold, color:C.bg, borderRadius:10,
            padding:"2px 9px", fontSize:12, fontWeight:800 }}>{unread}</span>}
        </div>
        {unread>0&&<button onClick={()=>setNotifs(p=>p.map(n=>({...n,read:true})))}
          style={{ background:"none", border:"none", cursor:"pointer", color:C.gold,
            fontSize:13, fontWeight:700, fontFamily:"inherit" }}>{t.notif.markAll}</button>}
      </div>
      {notifs.length===0
        ? <EmptyState icon="bell" title={t.notif.empty}/>
        : <div style={{ display:"flex", flexDirection:"column", gap:8 }}>
            {notifs.map(n=>{ const tp=TYPE[n.type]||TYPE.system; return (
              <div key={n.id} onClick={()=>setNotifs(p=>p.map(x=>x.id===n.id?{...x,read:true}:x))}
                style={{ background:n.read?C.surface:`${C.gold}08`,
                  border:`1px solid ${n.read?C.border:C.gold+"33"}`,
                  borderRadius:14, padding:"13px 15px", display:"flex", gap:12, cursor:"pointer" }}>
                <div style={{ width:38, height:38, borderRadius:11, flexShrink:0,
                  background:`${tp.col}18`, display:"flex", alignItems:"center", justifyContent:"center" }}>
                  <I n={tp.icon} s={16} c={tp.col}/>
                </div>
                <div style={{ flex:1 }}>
                  <div style={{ color:n.read?C.textSec:C.text, fontSize:13, lineHeight:1.55 }}>
                    {lang==="ar"?n.text:n.textEn}
                  </div>
                  <div style={{ color:C.textMuted, fontSize:11, marginTop:4 }}>{n.time} {t.ago}</div>
                </div>
                {!n.read&&<div style={{ width:9, height:9, borderRadius:"50%", background:C.gold,
                  flexShrink:0, marginTop:5, boxShadow:`0 0 6px ${C.gold}` }}/>}
              </div>
            ); })}
          </div>}
    </div>
  );
};
const SettingsPage = ({ t, lang, setLang, showToast }) => {
  const [shop,setShop]=useState({ name:"صالون أبو علي - بغداد", phone:"07701234567", address:"بغداد، الكرادة" });
  const [hours,setHours]=useState({ from:"09:00", to:"21:00" });
  const [notif,setNotif]=useState({ inApp:true, wa:true, sms:false, email:false });
  const [dep,setDep]=useState({ type:"none", value:0 });
  const [multiBarber,setMultiBarber]=useState(true);
  const [waOk,setWaOk]=useState(false);
  const [copied,setCopied]=useState(false);
  const link="https://cutpro.iq/book/abu-ali-baghdad";
  const Sec=({ icon, title, children })=>(
    <Card style={{ marginBottom:14 }}>
      <div style={{ display:"flex", alignItems:"center", gap:8, marginBottom:14,
        paddingBottom:12, borderBottom:`1px solid ${C.border}` }}>
        <div style={{ width:32, height:32, borderRadius:9, background:`${C.gold}18`,
          display:"flex", alignItems:"center", justifyContent:"center" }}>
          <I n={icon} s={15} c={C.gold}/>
        </div>
        <div style={{ fontWeight:800, color:C.text, fontSize:15 }}>{title}</div>
      </div>
      {children}
    </Card>
  );
  const NRow=({ k, label, icon })=>(
    <div style={{ display:"flex", alignItems:"center", justifyContent:"space-between",
      padding:"11px 0", borderBottom:`1px solid ${C.border}` }}>
      <div style={{ display:"flex", alignItems:"center", gap:10 }}>
        <I n={icon} s={16} c={notif[k]?C.gold:C.textMuted}/>
        <span style={{ color:C.text, fontSize:14 }}>{label}</span>
      </div>
      <Toggle on={notif[k]} onChange={v=>setNotif(p=>({...p,[k]:v}))}/>
    </div>
  );
  return (
    <div>
      <div style={{ fontSize:20, fontWeight:900, color:C.text, marginBottom:16 }}>{t.settings.title}</div>
      <Sec icon="edit" title={t.settings.profile}>
        <Inp label={t.settings.shopName} value={shop.name} onChange={v=>setShop(p=>({...p,name:v}))}/>
        <Inp label={t.settings.phone}    value={shop.phone} onChange={v=>setShop(p=>({...p,phone:v}))} type="tel"/>
        <Inp label={t.settings.address}  value={shop.address} onChange={v=>setShop(p=>({...p,address:v}))}/>
      </Sec>
      <Sec icon="wa" title={t.settings.whatsapp}>
        {waOk
          ? <div style={{ display:"flex", alignItems:"center", gap:10, padding:"10px 14px",
              background:C.greenFaint, borderRadius:11, border:`1px solid ${C.green}33` }}>
              <I n="check" s={18} c={C.green}/>
              <span style={{ color:C.green, fontWeight:700 }}>{t.settings.whatsappConnected}</span>
            </div>
          : <div>
              <div style={{ color:C.textSec, fontSize:13, marginBottom:12, lineHeight:1.6 }}>
                {lang==="ar"
                  ?"اربط واتساب بيزنس لاستقبال الحجوزات تلقائياً وإرسال التأكيدات والتذكيرات"
                  :"Connect WhatsApp Business to receive bookings automatically"}
              </div>
              {[
                lang==="ar"?"العميل يرسل رسالة واتساب 💬":"Customer sends WhatsApp message 💬",
                lang==="ar"?"النظام يحلل الطلب تلقائياً 🤖":"System parses booking automatically 🤖",
                lang==="ar"?"ينشأ طلب حجز في اللوحة 📋":"Booking request created in dashboard 📋",
                lang==="ar"?"تأكيد تلقائي على واتساب ✅":"Auto-confirmation sent via WhatsApp ✅",
              ].map((step,i)=>(
                <div key={i} style={{ display:"flex", gap:10, marginBottom:8 }}>
                  <div style={{ width:22, height:22, borderRadius:"50%", background:C.goldFaint,
                    border:`1px solid ${C.gold}44`, flexShrink:0, display:"flex",
                    alignItems:"center", justifyContent:"center", color:C.gold, fontSize:11, fontWeight:800 }}>{i+1}</div>
                  <span style={{ color:C.textSec, fontSize:13, paddingTop:2 }}>{step}</span>
                </div>
              ))}
              <Btn onClick={()=>{ setWaOk(true);showToast(lang==="ar"?"✓ تم ربط واتساب":"✓ WhatsApp connected"); }}
                v="success" full style={{ marginTop:14 }}>
                <div style={{ display:"flex", alignItems:"center", justifyContent:"center", gap:8 }}>
                  <I n="wa" s={17} c={C.green}/>{t.settings.whatsappConnect}
                </div>
              </Btn>
            </div>}
      </Sec>
      <Sec icon="link" title={t.settings.bookingLink}>
        <div style={{ color:C.textSec, fontSize:13, marginBottom:10 }}>
          {lang==="ar"?"شارك هذا الرابط مع عملائك":"Share this link with customers"}
        </div>
        <div style={{ display:"flex", gap:8, alignItems:"flex-start" }}>
          <div style={{ flex:1 }}>
            <Inp label="" value={link} onChange={()=>{}} readOnly/>
          </div>
          <button onClick={()=>{ setCopied(true);setTimeout(()=>setCopied(false),2000); }}
            style={{ background:copied?C.greenFaint:C.goldFaint,
              border:`1px solid ${copied?C.green:C.gold}44`, borderRadius:11,
              padding:"11px 12px", cursor:"pointer", color:copied?C.green:C.gold,
              fontWeight:700, fontSize:12, fontFamily:"inherit",
              display:"flex", alignItems:"center", gap:5, whiteSpace:"nowrap", flexShrink:0 }}>
            <I n={copied?"check":"copy"} s={14} c={copied?C.green:C.gold}/>
            {copied?t.settings.linkCopied:t.settings.copyLink}
          </button>
        </div>
      </Sec>
      <Sec icon="globe" title={t.settings.language}>
        <div style={{ display:"flex", gap:10 }}>
          {[["en","🇬🇧  English"],["ar","🇮🇶  العربية"]].map(([l,label])=>(
            <button key={l} onClick={()=>setLang(l)} style={{ flex:1, padding:"13px",
              borderRadius:12, cursor:"pointer", fontFamily:"inherit",
              border:`1.5px solid ${lang===l?C.gold:C.border}`,
              background:lang===l?C.goldFaint:C.surfaceMid,
              color:lang===l?C.gold:C.textSec, fontWeight:800, fontSize:15 }}>{label}</button>
          ))}
        </div>
      </Sec>
      <Sec icon="clock" title={t.settings.workHours}>
        <div style={{ display:"flex", gap:12 }}>
          <div style={{ flex:1 }}><Inp label={t.settings.from} value={hours.from}
            onChange={v=>setHours(p=>({...p,from:v}))} type="time"/></div>
          <div style={{ flex:1 }}><Inp label={t.settings.to} value={hours.to}
            onChange={v=>setHours(p=>({...p,to:v}))} type="time"/></div>
        </div>
      </Sec>
      <Sec icon="dollar" title={t.settings.depositSettings}>
        <div style={{ display:"flex", gap:8, marginBottom:dep.type!=="none"?14:0 }}>
          {[["none",t.settings.noDeposit],["fixed",t.settings.fixedDeposit],["percent",t.settings.percentDeposit]].map(([k,l])=>(
            <button key={k} onClick={()=>setDep(p=>({...p,type:k}))} style={{ flex:1, padding:"10px 4px",
              borderRadius:10, border:`1.5px solid ${dep.type===k?C.gold:C.border}`,
              background:dep.type===k?C.goldFaint:C.surfaceMid,
              color:dep.type===k?C.gold:C.textSec, fontWeight:700, fontSize:11,
              cursor:"pointer", fontFamily:"inherit" }}>{l}</button>
          ))}
        </div>
        {dep.type!=="none"&&<Inp
          label={dep.type==="fixed"?`${t.settings.depositValue} (د.ع)`:`${t.settings.depositValue} (%)`}
          value={String(dep.value)} onChange={v=>setDep(p=>({...p,value:Number(v)}))} type="number"/>}
      </Sec>
      <Card style={{ marginBottom:14 }}>
        <div style={{ display:"flex", alignItems:"center", justifyContent:"space-between" }}>
          <div style={{ display:"flex", alignItems:"center", gap:10 }}>
            <div style={{ width:32, height:32, borderRadius:9, background:`${C.gold}18`,
              display:"flex", alignItems:"center", justifyContent:"center" }}>
              <I n="users" s={15} c={C.gold}/>
            </div>
            <div>
              <div style={{ fontWeight:700, color:C.text, fontSize:14 }}>{t.settings.multiBarber}</div>
              <div style={{ color:C.textMuted, fontSize:12 }}>
                {multiBarber?(lang==="ar"?"مفعّل":"Enabled"):(lang==="ar"?"معطّل":"Disabled")}
              </div>
            </div>
          </div>
          <Toggle on={multiBarber} onChange={setMultiBarber}/>
        </div>
      </Card>
      <Sec icon="bell" title={t.settings.channels}>
        <NRow k="inApp" label={t.settings.inApp}    icon="bell"/>
        <NRow k="wa"    label={t.settings.whatsapp} icon="wa"  />
        <NRow k="sms"   label={t.settings.sms}      icon="phone"/>
        <NRow k="email" label={t.settings.email}    icon="globe"/>
      </Sec>
      <Btn onClick={()=>showToast(lang==="ar"?"✓ تم حفظ الإعدادات":"✓ Settings saved")} full
        style={{ padding:"15px", fontSize:16 }}>{t.settings.save}</Btn>
    </div>
  );
};

// ══════════════════════════════════════════════════════
//  AI TRAINING PAGE — تدريب الذكاء الاصطناعي
// ══════════════════════════════════════════════════════
const AITrainingPage = ({ lang, services, barbers, shopName, onClose, showToast }) => {
  const isRtl = lang === "ar";
  const lbl = (ar, en) => isRtl ? ar : en;

  const [step, setStep] = useState(1);
  const [trained, setTrained] = useState(false);
  const [loading, setLoading] = useState(false);
  const [msgs, setMsgs] = useState([]);
  const [input, setInput] = useState("");
  const [aiPersonality, setAiPersonality] = useState(isRtl
    ? "ودية وبالعراقي، استخدم كلمات مثل (هلو، عيني، أهلاً)"
    : "Friendly and professional");
  const [customRules, setCustomRules] = useState([]);
  const [newRule, setNewRule] = useState("");
  const [systemPrompt, setSystemPrompt] = useState("");
  const endRef = useRef(null);

  const PRESET_RULES = isRtl ? [
    "إذا الوقت محجوز، اعرض ٣ بدائل قريبة",
    "ذكّر الزبون بموعده قبل ساعة",
    "إذا ألغى الزبون، اسأله إذا يريد وقت ثاني",
    "لا تقبل حجوزات بعد وقت الدوام",
    "أعطِ خصم ١٠٪ لزبائن الجمعة",
  ] : [
    "If slot is taken, offer 3 nearby alternatives",
    "Remind customer 1 hour before appointment",
    "If cancelled, ask if they want to reschedule",
    "Don't accept bookings outside working hours",
    "Offer 10% discount for returning customers",
  ];

  useEffect(() => { endRef.current?.scrollIntoView({ behavior:"smooth" }); }, [msgs]);

  const buildSystemPrompt = () => {
    const svcList = services.map(s => `${isRtl?s.nameAr:s.name}: ${iqd(s.price)} (${s.duration} ${lbl("دقيقة","min")})`).join("
");
    const barbList = barbers.map(b => isRtl?b.name:b.nameEn).join("، ");
    return `أنت مساعد حجز ذكي لـ${shopName}.

الخدمات المتاحة:
${svcList}

الحلاقون: ${barbList}
ساعات العمل: 9 صباحاً — 9 مساءً
يوم العطلة: الجمعة

شخصيتك: ${aiPersonality}

القواعد الخاصة:
${customRules.map((r,i)=>`${i+1}. ${r}`).join("
")}

مهمتك:
- استقبل طلبات الحجز وحوّلها لموعد
- تحقق من توفر الوقت
- أرسل تأكيد بالتفاصيل الكاملة
- تذكر اسم الزبون واستخدمه في الردود`;
  };

  const sendTrainingMsg = async () => {
    if (!input.trim() || loading) return;
    const userText = input.trim();
    setInput("");
    setMsgs(p => [...p, { id:Date.now(), from:"owner", text:userText }]);
    setLoading(true);
    await new Promise(r => setTimeout(r, 1200));

    // Simulate AI learning response
    const responses = isRtl ? [
      `فهمت! ✓ سأتذكر هذا دائماً عند الرد على الزبائن.`,
      `تمام، سيكون هذا ضمن قواعدي الأساسية في كل محادثة.`,
      `ممتاز! حفظت هذا التوجيه وسأطبقه على جميع الطلبات.`,
      `شكراً للتوضيح. سأستخدم هذا الأسلوب مع كل زبون.`,
    ] : [
      "Got it! ✓ I'll remember this for all customer conversations.",
      "Perfect, I'll apply this rule in every booking request.",
      "Understood! This preference is now saved in my system.",
      "Great guidance! I'll use this style with every customer.",
    ];
    const reply = responses[Math.floor(Math.random() * responses.length)];
    setMsgs(p => [...p, { id:Date.now()+1, from:"ai", text:reply }]);
    setLoading(false);
  };

  const finalizeTrain = async () => {
    setLoading(true);
    const prompt = buildSystemPrompt();
    setSystemPrompt(prompt);
    await new Promise(r => setTimeout(r, 2000));
    setTrained(true);
    setLoading(false);
    showToast(lbl("✓ تم تدريب الذكاء الاصطناعي بنجاح!","✓ AI trained successfully!"));
  };

  return (
    <div style={{ position:"fixed", inset:0, background:C.bg, zIndex:3500, overflowY:"auto",
      direction:isRtl?"rtl":"ltr", fontFamily:"'Inter',-apple-system,sans-serif" }}>

      {/* Header */}
      <div style={{ background:C.surface, borderBottom:`1px solid ${C.border}`,
        padding:"14px 18px", display:"flex", alignItems:"center", justifyContent:"space-between",
        position:"sticky", top:0, zIndex:10 }}>
        <div style={{ display:"flex", alignItems:"center", gap:10 }}>
          <div style={{ width:38, height:38, borderRadius:11, background:`${C.purple}18`,
            display:"flex", alignItems:"center", justifyContent:"center" }}>
            <span style={{ fontSize:20 }}>🤖</span>
          </div>
          <div>
            <div style={{ fontWeight:900, fontSize:16, color:C.text }}>
              {lbl("تدريب الذكاء الاصطناعي","AI Training")}
            </div>
            <div style={{ color:trained?C.green:C.textSec, fontSize:11, display:"flex", alignItems:"center", gap:4 }}>
              <div style={{ width:6, height:6, borderRadius:"50%", background:trained?C.green:C.amber }}/>
              {trained ? lbl("مدرّب وجاهز","Trained & Ready") : lbl("قيد الإعداد","Setup in progress")}
            </div>
          </div>
        </div>
        <button onClick={onClose} style={{ background:C.surfaceHigh, border:"none",
          borderRadius:9, width:34, height:34, cursor:"pointer",
          display:"flex", alignItems:"center", justifyContent:"center" }}>
          <I n="x" s={16} c={C.textSec}/>
        </button>
      </div>

      {/* Step progress */}
      <div style={{ display:"flex", gap:0, borderBottom:`1px solid ${C.border}` }}>
        {[
          lbl("شخصية الـ AI","AI Personality"),
          lbl("القواعد","Rules"),
          lbl("التدريب","Training"),
          lbl("مراجعة","Review"),
        ].map((label, i) => (
          <div key={i} onClick={() => setStep(i+1)}
            style={{ flex:1, padding:"10px 4px", textAlign:"center", cursor:"pointer",
              borderBottom:`2px solid ${step===i+1?C.purple:"transparent"}`,
              color:step===i+1?C.purple:step>i+1?C.green:C.textMuted,
              fontSize:11, fontWeight:step===i+1?700:500, transition:"all .2s" }}>
            {step>i+1?"✓ ":""}{label}
          </div>
        ))}
      </div>

      <div style={{ padding:"20px 18px 100px", maxWidth:520, margin:"0 auto" }}>

        {/* STEP 1 — شخصية AI */}
        {step===1&&(
          <div style={{ animation:"fadeIn .3s ease" }}>
            <div style={{ fontWeight:800, fontSize:19, color:C.text, marginBottom:6 }}>
              {lbl("كيف تريد يرد الـ AI على زبائنك؟","How should AI talk to your customers?")}
            </div>
            <div style={{ color:C.textSec, fontSize:14, marginBottom:20, lineHeight:1.6 }}>
              {lbl(
                "حدد شخصية الذكاء الاصطناعي — أسلوب الرد، اللهجة، ودرجة الرسمية",
                "Define the AI personality — tone, style, and formality level"
              )}
            </div>

            {/* Preset personalities */}
            <div style={{ display:"grid", gridTemplateColumns:"1fr 1fr", gap:10, marginBottom:18 }}>
              {[
                { icon:"😊", label:lbl("ودي وعراقي","Friendly Iraqi"),
                  val:lbl("ودية وبالعراقي، استخدم: هلو، عيني، أهلاً، يا صديقي","Friendly and warm, use casual language") },
                { icon:"👔", label:lbl("رسمي ومحترف","Formal & Pro"),
                  val:lbl("رسمي ومحترف، استخدم لغة فصحى مهذبة","Formal and professional tone") },
                { icon:"⚡", label:lbl("سريع ومختصر","Quick & Direct"),
                  val:lbl("اجعل الردود قصيرة ومباشرة بدون كلام زائد","Short and direct responses only") },
                { icon:"🎭", label:lbl("مخصص","Custom"),
                  val:"custom" },
              ].map((p,i)=>(
                <div key={i} onClick={()=>{ if(p.val!=="custom") setAiPersonality(p.val); }}
                  style={{ background:aiPersonality===p.val?`${C.purple}18`:C.surfaceMid,
                    border:`1.5px solid ${aiPersonality===p.val?C.purple:C.border}`,
                    borderRadius:14, padding:"14px 12px", cursor:"pointer", textAlign:"center",
                    transition:"all .15s" }}>
                  <div style={{ fontSize:24, marginBottom:6 }}>{p.icon}</div>
                  <div style={{ fontWeight:700, color:C.text, fontSize:13 }}>{p.label}</div>
                </div>
              ))}
            </div>

            <div style={{ marginBottom:18 }}>
              <div style={{ color:C.textSec, fontSize:12, marginBottom:6, fontWeight:600 }}>
                {lbl("وصف الشخصية (يمكنك تعديله)","Personality description (editable)")}
              </div>
              <textarea value={aiPersonality} onChange={e=>setAiPersonality(e.target.value)}
                rows={3}
                style={{ width:"100%", background:C.surfaceMid, border:`1px solid ${C.border}`,
                  borderRadius:11, padding:"11px 14px", color:C.text, fontSize:14,
                  outline:"none", boxSizing:"border-box", fontFamily:"inherit",
                  resize:"none", lineHeight:1.6 }}
                onFocus={e=>e.target.style.borderColor=C.purple}
                onBlur={e=>e.target.style.borderColor=C.border}/>
            </div>

            <Btn onClick={()=>setStep(2)} full style={{ padding:"14px", background:C.purple, color:"#fff" }}>
              {lbl("التالي: القواعد الخاصة →","Next: Custom Rules →")}
            </Btn>
          </div>
        )}

        {/* STEP 2 — القواعد */}
        {step===2&&(
          <div style={{ animation:"fadeIn .3s ease" }}>
            <div style={{ fontWeight:800, fontSize:19, color:C.text, marginBottom:6 }}>
              {lbl("قواعد صالونك الخاصة","Your Shop Rules")}
            </div>
            <div style={{ color:C.textSec, fontSize:14, marginBottom:20 }}>
              {lbl("أضف قواعد خاصة بصالونك — الـ AI سيطبقها تلقائياً",
                   "Add custom rules — AI will apply them automatically")}
            </div>

            {/* Preset rules */}
            <div style={{ marginBottom:16 }}>
              <div style={{ color:C.textMuted, fontSize:11, fontWeight:700, marginBottom:8,
                textTransform:"uppercase", letterSpacing:"0.05em" }}>
                {lbl("قواعد جاهزة — انقر للإضافة","Preset rules — tap to add")}
              </div>
              <div style={{ display:"flex", flexDirection:"column", gap:6 }}>
                {PRESET_RULES.map((rule,i)=>{
                  const added = customRules.includes(rule);
                  return (
                    <div key={i} onClick={()=>{ if(!added) setCustomRules(p=>[...p,rule]);
                      else setCustomRules(p=>p.filter(r=>r!==rule)); }}
                      style={{ display:"flex", alignItems:"center", gap:10, padding:"10px 14px",
                        background:added?`${C.purple}15`:C.surfaceMid,
                        border:`1px solid ${added?C.purple:C.border}`,
                        borderRadius:10, cursor:"pointer", transition:"all .15s" }}>
                      <div style={{ width:20, height:20, borderRadius:6, flexShrink:0,
                        background:added?C.purple:C.surfaceHigh,
                        display:"flex", alignItems:"center", justifyContent:"center" }}>
                        {added&&<I n="check" s={12} c="#fff" sw={3}/>}
                      </div>
                      <span style={{ color:added?C.purple:C.textSec, fontSize:13 }}>{rule}</span>
                    </div>
                  );
                })}
              </div>
            </div>

            {/* Custom rule input */}
            <div style={{ display:"flex", gap:8, marginBottom:16 }}>
              <input value={newRule} onChange={e=>setNewRule(e.target.value)}
                onKeyDown={e=>{ if(e.key==="Enter"&&newRule.trim()){
                  setCustomRules(p=>[...p,newRule.trim()]); setNewRule(""); } }}
                placeholder={lbl("أضف قاعدة خاصة…","Add custom rule…")}
                style={{ flex:1, background:C.surfaceMid, border:`1px solid ${C.border}`,
                  borderRadius:10, padding:"10px 14px", color:C.text, fontSize:13,
                  outline:"none", fontFamily:"inherit" }}
                onFocus={e=>e.target.style.borderColor=C.purple}
                onBlur={e=>e.target.style.borderColor=C.border}/>
              <button onClick={()=>{ if(newRule.trim()){
                  setCustomRules(p=>[...p,newRule.trim()]); setNewRule(""); } }}
                style={{ background:C.purple, border:"none", borderRadius:10,
                  width:40, height:40, cursor:"pointer",
                  display:"flex", alignItems:"center", justifyContent:"center" }}>
                <I n="plus" s={18} c="#fff"/>
              </button>
            </div>

            {/* Added rules */}
            {customRules.length>0&&(
              <div style={{ marginBottom:18 }}>
                <div style={{ color:C.textMuted, fontSize:11, fontWeight:700, marginBottom:8 }}>
                  {lbl(`${customRules.length} قاعدة مضافة`,`${customRules.length} rules added`)}
                </div>
                {customRules.map((r,i)=>(
                  <div key={i} style={{ display:"flex", alignItems:"center", gap:8,
                    background:`${C.purple}10`, border:`1px solid ${C.purple}33`,
                    borderRadius:10, padding:"8px 12px", marginBottom:6 }}>
                    <div style={{ width:6, height:6, borderRadius:"50%", background:C.purple, flexShrink:0 }}/>
                    <span style={{ flex:1, color:C.text, fontSize:13 }}>{r}</span>
                    <button onClick={()=>setCustomRules(p=>p.filter((_,j)=>j!==i))}
                      style={{ background:"none", border:"none", cursor:"pointer", padding:2 }}>
                      <I n="x" s={14} c={C.red}/>
                    </button>
                  </div>
                ))}
              </div>
            )}

            <div style={{ display:"flex", gap:10 }}>
              <Btn onClick={()=>setStep(1)} v="ghost" style={{ flex:1 }}>{lbl("رجوع","Back")}</Btn>
              <Btn onClick={()=>setStep(3)} style={{ flex:2, background:C.purple, color:"#fff" }}>
                {lbl("التالي: التدريب →","Next: Training →")}
              </Btn>
            </div>
          </div>
        )}

        {/* STEP 3 — محادثة التدريب */}
        {step===3&&(
          <div style={{ animation:"fadeIn .3s ease" }}>
            <div style={{ fontWeight:800, fontSize:19, color:C.text, marginBottom:6 }}>
              {lbl("علّم الـ AI بأسلوبك","Teach the AI your way")}
            </div>
            <div style={{ color:C.textSec, fontSize:14, marginBottom:16, lineHeight:1.6 }}>
              {lbl(
                "اكتب أي توجيهات إضافية، أمثلة على الردود، أو مواقف خاصة تريد الـ AI يتعاملها بطريقة معينة",
                "Write additional instructions, example responses, or special scenarios you want AI to handle"
              )}
            </div>

            {/* Training chat */}
            <div style={{ background:C.surfaceMid, borderRadius:16, padding:14,
              height:240, overflowY:"auto", marginBottom:12, border:`1px solid ${C.border}` }}>
              {msgs.length===0&&(
                <div style={{ textAlign:"center", paddingTop:40, color:C.textMuted, fontSize:13 }}>
                  {lbl(
                    'مثال: "إذا الزبون كتب بالإنجليزي، رد بالإنجليزي"',
                    'Example: "If customer asks about price, always mention the discount"'
                  )}
                </div>
              )}
              {msgs.map(m=>(
                <div key={m.id} style={{ display:"flex",
                  justifyContent:m.from==="owner"?"flex-end":"flex-start",
                  marginBottom:8 }}>
                  <div style={{ maxWidth:"85%",
                    background:m.from==="owner"?C.purple:"#1F2C34",
                    borderRadius:12, padding:"9px 13px" }}>
                    <div style={{ color:"#fff", fontSize:13, lineHeight:1.5 }}>{m.text}</div>
                  </div>
                </div>
              ))}
              {loading&&(
                <div style={{ display:"flex", gap:5, padding:"8px 12px" }}>
                  {[0,1,2].map(i=>(
                    <div key={i} style={{ width:8, height:8, borderRadius:"50%",
                      background:C.purple, animation:`bounce .8s ${i*0.2}s infinite alternate` }}/>
                  ))}
                </div>
              )}
              <div ref={endRef}/>
            </div>

            <div style={{ display:"flex", gap:8, marginBottom:16 }}>
              <input value={input} onChange={e=>setInput(e.target.value)}
                onKeyDown={e=>e.key==="Enter"&&sendTrainingMsg()}
                placeholder={lbl("أكتب توجيهاً للـ AI…","Write an instruction for AI…")}
                style={{ flex:1, background:C.surfaceMid, border:`1px solid ${C.border}`,
                  borderRadius:10, padding:"10px 14px", color:C.text, fontSize:13,
                  outline:"none", fontFamily:"inherit" }}
                onFocus={e=>e.target.style.borderColor=C.purple}
                onBlur={e=>e.target.style.borderColor=C.border}/>
              <button onClick={sendTrainingMsg} disabled={!input.trim()||loading}
                style={{ background:C.purple, border:"none", borderRadius:10,
                  width:40, height:40, cursor:"pointer",
                  display:"flex", alignItems:"center", justifyContent:"center",
                  opacity:input.trim()?1:0.5 }}>
                <I n="trend" s={17} c="#fff"/>
              </button>
            </div>

            <div style={{ display:"flex", gap:10 }}>
              <Btn onClick={()=>setStep(2)} v="ghost" style={{ flex:1 }}>{lbl("رجوع","Back")}</Btn>
              <Btn onClick={()=>{ finalizeTrain(); setStep(4); }}
                style={{ flex:2, background:C.purple, color:"#fff" }}>
                {loading?lbl("جاري التدريب…","Training…"):lbl("إنهاء التدريب ✓","Finish Training ✓")}
              </Btn>
            </div>
          </div>
        )}

        {/* STEP 4 — مراجعة + تفعيل */}
        {step===4&&(
          <div style={{ animation:"fadeIn .3s ease" }}>
            {!trained?(
              <div style={{ textAlign:"center", padding:"40px 20px" }}>
                <div style={{ fontSize:48, marginBottom:16 }}>🤖</div>
                <div style={{ color:C.textSec, fontSize:16 }}>
                  {lbl("جاري تدريب الذكاء الاصطناعي…","Training AI model…")}
                </div>
                <div style={{ display:"flex", justifyContent:"center", gap:6, marginTop:16 }}>
                  {[0,1,2].map(i=>(
                    <div key={i} style={{ width:10, height:10, borderRadius:"50%",
                      background:C.purple, animation:`bounce .8s ${i*0.2}s infinite alternate` }}/>
                  ))}
                </div>
              </div>
            ):(
              <>
                <div style={{ textAlign:"center", marginBottom:24 }}>
                  <div style={{ width:80, height:80, borderRadius:24,
                    background:`${C.purple}18`, border:`2px solid ${C.purple}44`,
                    display:"flex", alignItems:"center", justifyContent:"center",
                    margin:"0 auto 16px", boxShadow:`0 0 30px ${C.purple}22` }}>
                    <span style={{ fontSize:38 }}>🤖</span>
                  </div>
                  <div style={{ fontWeight:900, fontSize:22, color:C.text, marginBottom:6 }}>
                    {lbl("الذكاء الاصطناعي جاهز! ✓","AI is Ready! ✓")}
                  </div>
                  <div style={{ color:C.textSec, fontSize:14 }}>
                    {lbl("سيبدأ الرد على زبائنك تلقائياً عند تفعيل واتساب",
                         "Will auto-reply to customers when WhatsApp is activated")}
                  </div>
                </div>

                {/* System prompt preview */}
                <Card style={{ marginBottom:16, background:C.surfaceMid }}>
                  <div style={{ fontWeight:700, color:C.text, fontSize:13, marginBottom:10 }}>
                    {lbl("الـ System Prompt المُولَّد","Generated System Prompt")}
                  </div>
                  <div style={{ background:C.bg, borderRadius:8, padding:"10px 12px",
                    fontFamily:"monospace", fontSize:11, color:C.textSec,
                    maxHeight:140, overflowY:"auto", lineHeight:1.6, direction:"ltr" }}>
                    {systemPrompt||buildSystemPrompt()}
                  </div>
                </Card>

                {/* Stats */}
                <div style={{ display:"grid", gridTemplateColumns:"repeat(3,1fr)", gap:8, marginBottom:18 }}>
                  {[
                    ["📋", customRules.length, lbl("قاعدة","Rules")],
                    ["✂️", services.length, lbl("خدمة","Services")],
                    ["💈", barbers.length, lbl("حلاق","Barbers")],
                  ].map(([icon,val,label],i)=>(
                    <div key={i} style={{ background:C.surface, border:`1px solid ${C.border}`,
                      borderRadius:12, padding:"12px 8px", textAlign:"center" }}>
                      <div style={{ fontSize:20, marginBottom:4 }}>{icon}</div>
                      <div style={{ color:C.purple, fontWeight:900, fontSize:18 }}>{val}</div>
                      <div style={{ color:C.textMuted, fontSize:11 }}>{label}</div>
                    </div>
                  ))}
                </div>

                <Btn onClick={onClose} full style={{ padding:"14px", background:C.purple, color:"#fff", fontSize:15 }}>
                  {lbl("تفعيل الآن 🚀","Activate Now 🚀")}
                </Btn>
              </>
            )}
          </div>
        )}
      </div>

      <style>{`
        @keyframes bounce{ from{transform:translateY(0)} to{transform:translateY(-5px)} }
      `}</style>
    </div>
  );
};


const SuperAdminPanel = ({ t, lang, onClose }) => {
  const [shops,setShops]=useState(ADMIN_SHOPS);
  const [open,setOpen]=useState(false);
  const [form,setForm]=useState({ name:"", owner:"", plan:"Basic" });
  const toggle=id=>setShops(p=>p.map(s=>s.id===id?{...s,status:s.status==="active"?"suspended":"active"}:s));
  const del=id=>setShops(p=>p.filter(s=>s.id!==id));
  return (
    <div style={{ position:"fixed", inset:0, background:C.bg, zIndex:9000, overflowY:"auto",
      fontFamily:"'Inter',-apple-system,sans-serif", direction:lang==="ar"?"rtl":"ltr" }}>
      <div style={{ background:"#100A00", borderBottom:`1px solid ${C.gold}44`,
        padding:"14px 18px", display:"flex", alignItems:"center", justifyContent:"space-between",
        position:"sticky", top:0, zIndex:10 }}>
        <div style={{ display:"flex", alignItems:"center", gap:10 }}>
          <div style={{ width:34, height:34, borderRadius:10, background:`${C.gold}18`,
            display:"flex", alignItems:"center", justifyContent:"center" }}>
            <I n="shield" s={18} c={C.gold}/>
          </div>
          <div>
            <div style={{ fontWeight:900, color:C.gold, fontSize:16 }}>{t.admin.title}</div>
            <div style={{ color:C.textMuted, fontSize:10 }}>SUPER ADMIN · RESTRICTED</div>
          </div>
        </div>
        <button onClick={onClose} style={{ background:C.surfaceHigh, border:"none",
          borderRadius:8, width:34, height:34, cursor:"pointer",
          display:"flex", alignItems:"center", justifyContent:"center" }}>
          <I n="x" s={16} c={C.textSec}/>
        </button>
      </div>
      <div style={{ padding:"18px 16px 80px", maxWidth:640, margin:"0 auto" }}>
        <div style={{ display:"grid", gridTemplateColumns:"repeat(3,1fr)", gap:8, marginBottom:18 }}>
          {[[shops.length,lang==="ar"?"إجمالي المحلات":"Total Shops",C.gold],
            [shops.filter(s=>s.status==="active").length,lang==="ar"?"نشط":"Active",C.green],
            [shops.filter(s=>s.status==="suspended").length,lang==="ar"?"موقوف":"Suspended",C.red]].map(([v,l,c],i)=>(
            <div key={i} style={{ background:C.surface, border:`1px solid ${C.border}`,
              borderRadius:13, padding:"14px 10px", textAlign:"center" }}>
              <div style={{ color:c, fontWeight:900, fontSize:22 }}>{v}</div>
              <div style={{ color:C.textMuted, fontSize:11, marginTop:3 }}>{l}</div>
            </div>
          ))}
        </div>
        <div style={{ display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:12 }}>
          <div style={{ fontWeight:800, color:C.text, fontSize:16 }}>{t.admin.shops}</div>
          <Btn onClick={()=>setOpen(true)} style={{ padding:"8px 13px", fontSize:13,
            display:"flex", alignItems:"center", gap:6 }}>
            <I n="plus" s={14} c={C.bg}/>{t.admin.addShop}
          </Btn>
        </div>
        <div style={{ display:"flex", flexDirection:"column", gap:10 }}>
          {shops.map(s=>(
            <Card key={s.id}>
              <div style={{ display:"flex", alignItems:"center", gap:12, marginBottom:12 }}>
                <Av char={s.name[0]} size={42} bg={s.status==="active"?C.gold:C.textMuted}/>
                <div style={{ flex:1 }}>
                  <div style={{ fontWeight:800, color:C.text }}>{s.name}</div>
                  <div style={{ color:C.textSec, fontSize:12, marginTop:2,
                    display:"flex", alignItems:"center", gap:4 }}>
                    <I n="phone" s={11} c={C.textMuted}/>{s.owner}
                  </div>
                </div>
                <span style={{ background:s.status==="active"?C.greenFaint:C.redFaint,
                  color:s.status==="active"?C.green:C.red,
                  padding:"3px 10px", borderRadius:20, fontSize:11, fontWeight:700 }}>
                  {s.status==="active"?t.admin.active:t.admin.suspended}
                </span>
              </div>
              <div style={{ display:"flex", gap:8, borderTop:`1px solid ${C.border}`, paddingTop:12 }}>
                <div style={{ flex:1, textAlign:"center" }}>
                  <div style={{ color:C.textMuted, fontSize:10, fontWeight:600 }}>{t.admin.plan}</div>
                  <div style={{ color:C.gold, fontWeight:800, fontSize:13, marginTop:2 }}>{s.plan}</div>
                </div>
                <div style={{ flex:1, textAlign:"center" }}>
                  <div style={{ color:C.textMuted, fontSize:10, fontWeight:600 }}>{lang==="ar"?"مواعيد":"Appts"}</div>
                  <div style={{ color:C.text, fontWeight:800, fontSize:13, marginTop:2 }}>{s.appts}</div>
                </div>
                <div style={{ flex:2, textAlign:"center" }}>
                  <div style={{ color:C.textMuted, fontSize:10, fontWeight:600 }}>{t.admin.expiry}</div>
                  <div style={{ color:C.text, fontWeight:800, fontSize:12, marginTop:2 }}>{s.expiry}</div>
                </div>
              </div>
              <div style={{ display:"flex", gap:8, marginTop:12 }}>
                <Btn onClick={()=>toggle(s.id)}
                  v={s.status==="active"?"danger":"success"} style={{ flex:1, padding:"8px" }}>
                  {s.status==="active"?t.admin.suspend:t.admin.activate}
                </Btn>
                <Btn onClick={()=>del(s.id)} v="danger" style={{ padding:"8px 14px" }}>
                  <I n="trash" s={14} c={C.red}/>
                </Btn>
              </div>
            </Card>
          ))}
        </div>
      </div>
      <Modal open={open} onClose={()=>setOpen(false)} title={t.admin.newShop}>
        <Inp label={t.admin.shopName} value={form.name} onChange={v=>setForm(p=>({...p,name:v}))}/>
        <Inp label={t.admin.ownerPhone} value={form.owner} onChange={v=>setForm(p=>({...p,owner:v}))} type="tel"/>
        <Sel label={t.admin.plan} value={form.plan} onChange={v=>setForm(p=>({...p,plan:v}))}
          options={[{v:"Basic",l:"Basic"},{v:"Pro",l:"Pro"},{v:"Enterprise",l:"Enterprise"}]}/>
        <div style={{ display:"flex", gap:10 }}>
          <Btn onClick={()=>setOpen(false)} v="ghost" style={{ flex:1 }}>{t.modal.cancel}</Btn>
          <Btn onClick={()=>{ if(!form.name.trim()) return;
            setShops(p=>[...p,{id:Date.now(),...form,status:"active",expiry:"2025-12-31",appts:0}]);
            setOpen(false); }} disabled={!form.name.trim()} style={{ flex:2 }}>{t.admin.addShop}</Btn>
        </div>
      </Modal>
    </div>
  );
};
export default function App() {
  const [lang,setLang]=useState("ar");
  const [page,setPage]=useState("dashboard");
  const [appts,setAppts]=useState(APPTS_INIT);
  const [customers,setCustomers]=useState(CUSTOMERS);
  const [services,setServices]=useState(SERVICES_INIT);
  const [barbers,setBarbers]=useState(BARBERS_INIT);
  const [notifs,setNotifs]=useState(NOTIFS_INIT);
  const [toast,setToast]=useState(null);
  const [bookOpen,setBookOpen]=useState(false);
  const [showBook,setShowBook]=useState(false);
  const [showWA,setShowWA]=useState(false);
  const [showAITrain,setShowAITrain]=useState(false);
  const [showAdmin,setShowAdmin]=useState(false);
  const tapRef=useRef(0); const tapTimer=useRef(null);

  const t=T[lang];
  const pendingCnt=appts.filter(a=>a.status==="pending").length;
  const unreadCnt=notifs.filter(n=>!n.read).length;

  const showToast=(msg,type="success")=>{ setToast({msg,type}); setTimeout(()=>setToast(null),3000); };

  const handleAction=(action,id)=>{
    setAppts(p=>p.map(a=>a.id===id?{...a,status:action==="accept"?"confirmed":"cancelled"}:a));
    if(action==="accept") setNotifs(p=>[{id:Date.now(),type:"booking",
      text:"تم تأكيد الموعد ✓",textEn:"Appointment confirmed ✓",time:"الآن",read:false},...p]);
    showToast(action==="accept"?(t.dir==="rtl"?"✓ تم القبول":"✓ Confirmed"):(t.dir==="rtl"?"تم الرفض":"Rejected"),
      action==="accept"?"success":"error");
  };

  const logoTap=()=>{
    tapRef.current++;
    clearTimeout(tapTimer.current);
    tapTimer.current=setTimeout(()=>{ tapRef.current=0; },2000);
    if(tapRef.current>=5){ tapRef.current=0; setShowAdmin(true); }
  };

  useEffect(()=>{ document.documentElement.dir=t.dir; },[t.dir]);

  const depSet={ type:"none", value:0 };

  const NAV=[
    { id:"dashboard",     icon:"home",      label:t.nav.dashboard,     badge:0         },
    { id:"bookings",      icon:"calendar",  label:t.nav.bookings,      badge:pendingCnt},
    { id:"customers",     icon:"users",     label:t.nav.customers,     badge:0         },
    { id:"services",      icon:"scissors",  label:t.nav.services,      badge:0         },
    { id:"finance",       icon:"dollar",    label:t.nav.finance,       badge:0         },
    { id:"barbers",       icon:"users",     label:t.nav.barbers,       badge:0         },
    { id:"notifications", icon:"bell",      label:t.nav.notifications, badge:unreadCnt },
    { id:"settings",      icon:"settings",  label:t.nav.settings,      badge:0         },
  ];

  const PAGES={
    dashboard:     <DashboardPage t={t} lang={lang} appts={appts} customers={customers}
                     services={services} barbers={barbers} onAction={handleAction}
                     onNewBooking={()=>setBookOpen(true)}/>,
    bookings:      <BookingsPage t={t} appts={appts} setAppts={setAppts} customers={customers}
                     services={services} barbers={barbers} showToast={showToast}/>,
    customers:     <CustomersPage t={t} customers={customers} setCustomers={setCustomers}
                     appts={appts} showToast={showToast}/>,
    services:      <ServicesPage t={t} services={services} setServices={setServices} showToast={showToast}/>,
    finance:       <FinancePage t={t} lang={lang} appts={appts}/>,
    barbers:       <BarbersPage t={t} barbers={barbers} setBarbers={setBarbers} showToast={showToast}/>,
    notifications: <NotificationsPage t={t} lang={lang} notifs={notifs} setNotifs={setNotifs}/>,
    settings:      <SettingsPage t={t} lang={lang} setLang={setLang} showToast={showToast}/>,
  };

  return (
    <div style={{ minHeight:"100vh", background:C.bg,
      fontFamily:"'Inter',-apple-system,BlinkMacSystemFont,sans-serif",
      color:C.text, direction:t.dir }}>
      <style>{`
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap');
        *{box-sizing:border-box;margin:0;padding:0;}
        input[type=time]::-webkit-calendar-picker-indicator,
        input[type=date]::-webkit-calendar-picker-indicator{filter:invert(.4)sepia(1)hue-rotate(35deg);}
        ::-webkit-scrollbar{width:4px;height:4px;}
        ::-webkit-scrollbar-thumb{background:#333;border-radius:2px;}
        select option{background:#1E1E21;}
        @keyframes toastIn{from{transform:translate(-50%,16px);opacity:0}to{transform:translate(-50%,0);opacity:1}}
        /* PWA — add to manifest.json: display:standalone, theme_color:#0C0C0D */
        @keyframes fadeIn{from{opacity:0}to{opacity:1}}
        @keyframes slideUp{from{transform:translateY(100%)}to{transform:translateY(0)}}
        .dnb{transition:all .15s;} .dnb:hover{background:rgba(245,200,66,0.1)!important;}
        @media(max-width:767px){
          .dsb{display:none!important;}
          .mltr{margin-left:0!important;}
          .mrtl{margin-right:0!important;}
        }
        @media(min-width:768px){
          .mtb{display:none!important;}
          .mbn{display:none!important;}
          .mltr{margin-left:230px;}
          .mrtl{margin-right:230px;}
        }
      `}</style>

      {/* DESKTOP SIDEBAR */}
      <div className="dsb" style={{ position:"fixed", top:0,
        [t.dir==="rtl"?"right":"left"]:0, width:230, height:"100vh",
        background:C.surface,
        borderRight:t.dir==="ltr"?`1px solid ${C.border}`:"none",
        borderLeft:t.dir==="rtl"?`1px solid ${C.border}`:"none",
        display:"flex", flexDirection:"column", zIndex:10 }}>
        <div onClick={logoTap} style={{ padding:"18px 18px 14px",
          borderBottom:`1px solid ${C.border}`, cursor:"default", userSelect:"none" }}>
          <div style={{ display:"flex", alignItems:"center", gap:11 }}>
            <div style={{ width:40, height:40, borderRadius:12, background:`${C.gold}18`,
              border:`1.5px solid ${C.gold}44`, display:"flex", alignItems:"center", justifyContent:"center" }}>
              <I n="scissors" s={20} c={C.gold}/>
            </div>
            <div>
              <div style={{ fontWeight:900, fontSize:17, letterSpacing:"-0.02em" }}>CutPro</div>
              <div style={{ fontSize:10, color:C.textMuted, letterSpacing:"0.04em" }}>IRAQ · د.ع</div>
            </div>
          </div>
        </div>
        <nav style={{ flex:1, padding:"10px 10px", overflowY:"auto" }}>
          {NAV.map(item=>(
            <button key={item.id} className="dnb" onClick={()=>setPage(item.id)} style={{
              width:"100%", display:"flex", alignItems:"center", gap:10,
              padding:"10px 12px", borderRadius:11, border:"none", cursor:"pointer",
              marginBottom:2, fontFamily:"inherit",
              background:page===item.id?`${C.gold}18`:"transparent",
              color:page===item.id?C.gold:C.textSec,
              fontWeight:page===item.id?700:500, fontSize:14,
              textAlign:t.dir==="rtl"?"right":"left" }}>
              <I n={item.icon} s={17} c={page===item.id?C.gold:C.textSec}/>
              <span style={{ flex:1 }}>{item.label}</span>
              {item.badge>0&&<span style={{ background:C.gold, color:C.bg,
                borderRadius:10, padding:"1px 7px", fontSize:10, fontWeight:900 }}>{item.badge}</span>}
            </button>
          ))}
          <button className="dnb" onClick={()=>setShowBook(true)} style={{
            width:"100%", display:"flex", alignItems:"center", gap:10,
            padding:"10px 12px", borderRadius:11, border:`1px solid ${C.green}33`,
            cursor:"pointer", marginTop:8, fontFamily:"inherit",
            background:`${C.green}08`, color:C.green, fontWeight:600, fontSize:13 }}>
            <I n="globe" s={17} c={C.green}/>
            <span>{t.nav.bookingPage}</span>
          </button>
          <button className="dnb" onClick={()=>setShowWA(true)} style={{
            width:"100%", display:"flex", alignItems:"center", gap:10,
            padding:"10px 12px", borderRadius:11, border:`1px solid #25D36633`,
            cursor:"pointer", marginTop:6, fontFamily:"inherit",
            background:"#0B221720", color:"#25D366", fontWeight:600, fontSize:13 }}>
            <I n="wa" s={17} c="#25D366"/>
            <span>{lang==="ar"?"محاكاة واتساب AI":"WhatsApp AI Sim"}</span>
          </button>
          <button className="dnb" onClick={()=>setShowAITrain(true)} style={{
            width:"100%", display:"flex", alignItems:"center", gap:10,
            padding:"10px 12px", borderRadius:11,
            border:`1px solid ${C.purple}33`,
            cursor:"pointer", marginTop:6, fontFamily:"inherit",
            background:`${C.purple}08`, color:C.purple, fontWeight:600, fontSize:13 }}>
            <span style={{ fontSize:16 }}>🤖</span>
            <span>{lang==="ar"?"تدريب الذكاء الاصطناعي":"Train AI"}</span>
          </button>
        </nav>
        <div style={{ padding:"12px 18px", borderTop:`1px solid ${C.border}` }}>
          <div style={{ display:"flex", alignItems:"center", gap:10 }}>
            <Av char="ع" size={34} bg={C.gold}/>
            <div style={{ flex:1, minWidth:0 }}>
              <div style={{ fontWeight:700, fontSize:13 }}>صالون أبو علي</div>
              <div style={{ fontSize:11, color:C.textMuted }}>بغداد، العراق 🇮🇶</div>
            </div>
          </div>
        </div>
      </div>

      {/* MOBILE TOPBAR */}
      <div className="mtb" style={{ position:"sticky", top:0, zIndex:10,
        background:`${C.bg}e8`, backdropFilter:"blur(20px)",
        borderBottom:`1px solid ${C.border}`,
        padding:"11px 15px", display:"flex",
        alignItems:"center", justifyContent:"space-between" }}>
        <div onClick={logoTap} style={{ display:"flex", alignItems:"center", gap:9 }}>
          <I n="scissors" s={17} c={C.gold}/>
          <span style={{ fontWeight:900, fontSize:16, letterSpacing:"-0.02em" }}>CutPro</span>
          <span style={{ fontSize:10, color:C.textMuted, fontWeight:600 }}>د.ع</span>
        </div>
        <div style={{ display:"flex", alignItems:"center", gap:7 }}>
          <button onClick={()=>setShowAITrain(true)} style={{ background:`${C.purple}18`,
            border:`1px solid ${C.purple}33`, borderRadius:8, padding:"6px 9px",
            color:C.purple, cursor:"pointer", fontSize:11, fontWeight:700, fontFamily:"inherit",
            display:"flex", alignItems:"center", gap:4 }}>
            🤖 {lang==="ar"?"AI":"AI"}
          </button>
          <button onClick={()=>setShowWA(true)} style={{ background:"#0B2217",
            border:"1px solid #25D36633", borderRadius:8, padding:"6px 9px",
            color:"#25D366", cursor:"pointer", fontSize:11, fontWeight:700, fontFamily:"inherit",
            display:"flex", alignItems:"center", gap:4 }}>
            <I n="wa" s={11} c="#25D366"/>WA AI
          </button>
          <button onClick={()=>setShowBook(true)} style={{ background:C.greenFaint,
            border:`1px solid ${C.green}33`, borderRadius:8, padding:"6px 9px",
            color:C.green, cursor:"pointer", fontSize:11, fontWeight:700, fontFamily:"inherit",
            display:"flex", alignItems:"center", gap:4 }}>
            <I n="globe" s={11} c={C.green}/>{lang==="ar"?"حجز عملاء":"Book"}
          </button>
          <button onClick={()=>setLang(l=>l==="en"?"ar":"en")} style={{
            background:C.surfaceHigh, border:`1px solid ${C.border}`,
            borderRadius:8, padding:"6px 10px", color:C.textSec,
            cursor:"pointer", fontSize:12, fontWeight:800, fontFamily:"inherit" }}>
            {lang==="en"?"AR":"EN"}
          </button>
          <div style={{ position:"relative" }}>
            <button onClick={()=>setPage("notifications")} style={{
              background:C.surfaceHigh, border:`1px solid ${C.border}`,
              borderRadius:8, width:34, height:34, cursor:"pointer",
              display:"flex", alignItems:"center", justifyContent:"center" }}>
              <I n="bell" s={15} c={C.textSec}/>
            </button>
            {unreadCnt>0&&<div style={{ position:"absolute", top:-4, right:-4, width:17, height:17,
              borderRadius:"50%", background:C.gold, border:`2px solid ${C.bg}`,
              fontSize:9, fontWeight:900, color:C.bg,
              display:"flex", alignItems:"center", justifyContent:"center" }}>{unreadCnt}</div>}
          </div>
        </div>
      </div>

      {/* MAIN CONTENT */}
      <div className={t.dir==="ltr"?"mltr":"mrtl"}
        style={{ minHeight:"100vh", paddingBottom:90 }}>
        <div style={{ padding:"14px 15px 0", maxWidth:680, margin:"0 auto" }}>
          {PAGES[page]}
        </div>
      </div>

      {/* MOBILE BOTTOM NAV */}
      <div className="mbn" style={{ position:"fixed", bottom:0, left:0, right:0, zIndex:10,
        background:`${C.surface}f5`, backdropFilter:"blur(24px)",
        borderTop:`1px solid ${C.border}`,
        display:"flex", padding:"7px 0 max(7px,env(safe-area-inset-bottom))" }}>
        {NAV.slice(0,5).map(item=>(
          <button key={item.id} onClick={()=>setPage(item.id)} style={{
            flex:1, display:"flex", flexDirection:"column", alignItems:"center", gap:3,
            background:"none", border:"none", cursor:"pointer", padding:"4px 2px",
            color:page===item.id?C.gold:C.textMuted,
            fontFamily:"inherit", position:"relative" }}>
            {page===item.id&&<div style={{ position:"absolute", top:-7, left:"50%",
              transform:"translateX(-50%)", width:22, height:3,
              borderRadius:"0 0 3px 3px", background:C.gold }}/>}
            <I n={item.icon} s={20} c={page===item.id?C.gold:C.textMuted}/>
            <span style={{ fontSize:9, fontWeight:page===item.id?700:500 }}>{item.label}</span>
            {item.badge>0&&<div style={{ position:"absolute", top:1, right:"calc(50% - 16px)",
              width:15, height:15, borderRadius:"50%", background:C.gold,
              border:`2px solid ${C.surface}`, fontSize:8, fontWeight:900, color:C.bg,
              display:"flex", alignItems:"center", justifyContent:"center" }}>{item.badge}</div>}
          </button>
        ))}
      </div>

      {/* Global booking modal */}
      <BookingModal open={bookOpen} onClose={()=>setBookOpen(false)}
        customers={customers} services={services} barbers={barbers} t={t} depSet={depSet}
        onSave={a=>{ setAppts(p=>[...p,a]);
          showToast(t.dir==="rtl"?"✓ تم إنشاء الحجز":"✓ Booking created"); }}/>

      {/* Public booking page */}
      {showBook&&<PublicBookingPage services={services} barbers={barbers}
        onClose={()=>setShowBook(false)} shopName="صالون أبو علي - بغداد" lang={lang}/>}

      {/* AI Training Page */}
      {showAITrain&&<AITrainingPage lang={lang} services={services} barbers={barbers}
        shopName={lang==="ar"?"صالون أبو علي":"Abu Ali Barber"}
        onClose={()=>setShowAITrain(false)} showToast={showToast}/>}

      {/* WhatsApp AI Simulator */}}
      {showWA&&<WhatsAppAIPage services={services} barbers={barbers} lang={lang}
        shopName={lang==="ar"?"صالون أبو علي":"Abu Ali Barber"}
        onClose={()=>setShowWA(false)}
        onBookingCreated={a=>{ setAppts(p=>[...p,a]);
          showToast(lang==="ar"?"📱 حجز جديد عبر واتساب!":"📱 New WhatsApp booking!"); }}/>}

      {/* Super admin (hidden — tap logo 5×) */}
      {showAdmin&&<SuperAdminPanel t={t} lang={lang} onClose={()=>setShowAdmin(false)}/>}

      {toast&&<Toast msg={toast.msg} type={toast.type} onClose={()=>setToast(null)}/>}
    </div>
  );
}
