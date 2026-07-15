#!/usr/bin/env python3
import os
DIST="/Users/LAVORO/giuseppe-build/dist"
BASE="https://giuseppebonellitattoo.art"

CSS = """
*{margin:0;padding:0;box-sizing:border-box}html{scroll-behavior:smooth}
body{background:#0a0908;color:#ece6da;font-family:'Inter',sans-serif;font-weight:300;line-height:1.6;-webkit-font-smoothing:antialiased;overflow-x:hidden}
img{display:block;max-width:100%}a{color:inherit}.gold{color:#c9a24b}
nav{position:fixed;top:0;left:0;right:0;z-index:50;display:flex;justify-content:space-between;align-items:center;padding:16px 22px;background:rgba(10,9,8,.86);backdrop-filter:blur(10px);border-bottom:1px solid rgba(201,162,75,.16)}
nav .logo{font-family:'Cormorant Garamond',serif;font-size:16px;letter-spacing:3px}
nav a.cta{font-size:11px;letter-spacing:2px;text-transform:uppercase;color:#c9a24b;text-decoration:none;border:1px solid rgba(201,162,75,.5);padding:9px 16px;border-radius:2px}
.hero{position:relative;min-height:78svh;display:flex;align-items:flex-end;overflow:hidden}
.hero .bg{position:absolute;inset:0}.hero .bg img{width:100%;height:100%;object-fit:cover;object-position:60% 45%;filter:contrast(1.05)}
.hero::after{content:"";position:absolute;inset:0;background:linear-gradient(0deg,rgba(8,7,6,.96) 4%,rgba(8,7,6,.4) 50%,rgba(8,7,6,.2));z-index:1}
.hero .in{position:relative;z-index:2;padding:0 22px 56px;max-width:1100px;margin:0 auto;width:100%}
.kick{font-size:11px;letter-spacing:5px;text-transform:uppercase;color:#c9a24b;margin-bottom:14px}
h1{font-family:'Cormorant Garamond',serif;font-weight:600;font-size:clamp(38px,8vw,80px);line-height:.98}
.lead{margin-top:18px;max-width:640px;color:#d3cabb;font-size:16px}
.btn{display:inline-block;margin-top:26px;background:#c9a24b;color:#191409;font-weight:500;padding:15px 30px;font-size:11px;letter-spacing:2px;text-transform:uppercase;text-decoration:none;border-radius:2px;border:0;cursor:pointer;font-family:inherit}
.btn:hover{transform:translateY(-2px)}
.wrap{max-width:1100px;margin:0 auto;padding:64px 22px}
.eyebrow{font-size:11px;letter-spacing:5px;text-transform:uppercase;color:#c9a24b;margin-bottom:12px}
h2{font-family:'Cormorant Garamond',serif;font-weight:500;font-size:clamp(26px,5vw,40px);line-height:1.1;margin-bottom:14px}
p.body{color:#8d8475;font-size:15px;max-width:720px}
.grid{display:grid;grid-template-columns:repeat(2,1fr);gap:10px;margin-top:30px}
.grid .c{aspect-ratio:3/4;overflow:hidden;border-radius:4px;background:#161310}
.grid img{width:100%;height:100%;object-fit:cover;transition:transform .8s}.grid .c:hover img{transform:scale(1.06)}
.info{display:grid;grid-template-columns:1fr;gap:22px;margin-top:30px}
.info .b{border:1px solid rgba(201,162,75,.16);border-radius:8px;padding:20px;background:#100d0a}
.info .b h3{font-family:'Cormorant Garamond',serif;font-weight:500;font-size:19px;margin-bottom:8px}
.info .b p{color:#8d8475;font-size:14px}
.faqs{margin-top:26px;max-width:760px}
.faqs details{border-bottom:1px solid rgba(236,230,218,.12)}
.faqs summary{cursor:pointer;list-style:none;padding:16px 28px 16px 0;font-size:16px;position:relative;font-family:'Cormorant Garamond',serif;font-weight:500}
.faqs summary::-webkit-details-marker{display:none}
.faqs summary::after{content:"+";position:absolute;right:2px;top:14px;color:#c9a24b;font-size:20px}
.faqs details[open] summary::after{content:"–"}
.faqs p{color:#8d8475;font-size:14px;padding:0 0 16px}
.formwrap{border:1px solid rgba(201,162,75,.22);border-radius:12px;padding:26px;background:#100d0a;margin-top:14px;max-width:720px}
.formwrap h2{margin-bottom:4px}.formwrap .s{color:#8d8475;font-size:14px;margin-bottom:20px}
.row{display:grid;grid-template-columns:1fr;gap:12px;margin-bottom:12px}
label{display:block;font-size:10px;letter-spacing:2px;text-transform:uppercase;color:#8d8475;margin-bottom:6px}
input,select,textarea{width:100%;background:#0a0807;border:1px solid rgba(236,230,218,.16);color:#ece6da;padding:13px 14px;border-radius:6px;font-family:inherit;font-size:16px}
input:focus,select:focus,textarea:focus{outline:0;border-color:#c9a24b}
textarea{min-height:90px;resize:vertical}
.ok{display:none;color:#7fe3c0;font-size:14px;margin-top:12px}
.note{font-size:11px;color:#8d8475;margin-top:10px}
footer{border-top:1px solid rgba(236,230,218,.1);padding:36px 22px;text-align:center;color:#8d8475;font-size:13px}
footer a{color:#c9a24b;text-decoration:none;margin:0 6px}
@media(min-width:820px){.grid{grid-template-columns:repeat(4,1fr)}.info{grid-template-columns:repeat(3,1fr)}.row.two{grid-template-columns:1fr 1fr}}
"""

PIXEL = """<script>!function(f,b,e,v,n,t,s){if(f.fbq)return;n=f.fbq=function(){n.callMethod?n.callMethod.apply(n,arguments):n.queue.push(arguments)};if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';n.queue=[];t=b.createElement(e);t.async=!0;t.src=v;s=b.getElementsByTagName(e)[0];s.parentNode.insertBefore(t,s)}(window,document,'script','https://connect.facebook.net/en_US/fbevents.js');
var FB_PIXEL_ID='__PIXEL_ID__';if(FB_PIXEL_ID&&FB_PIXEL_ID.indexOf('_')<0){fbq('init',FB_PIXEL_ID);fbq('track','PageView');}</script>"""

def imgs_html(names):
    return "\n".join(f'<div class="c"><img loading="lazy" src="/img/{n}.webp" alt="{alt}"></div>' for n,alt in names)

def faq_schema(faqs):
    items=",".join('{"@type":"Question","name":"%s","acceptedAnswer":{"@type":"Answer","text":"%s"}}'%(q.replace('"',"'"),a.replace('"',"'")) for q,a in faqs)
    return '{"@type":"FAQPage","mainEntity":[%s]}'%items

def page(slug,title,desc,kick,h1,lead,sections,gallery,faqs,form_title,form_src,extra_schema):
    canonical=f"{BASE}/{slug}/"
    kick_low=kick.lower()
    g=imgs_html(gallery)
    sec_html="\n".join('<div class="b"><h3>%s</h3><p>%s</p></div>'%(t,b) for t,b in sections)
    fa="\n".join(f'<details><summary>{q}</summary><p>{a}</p></details>' for q,a in faqs)
    schema='{"@context":"https://schema.org","@graph":[%s,%s,{"@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"%s/"},{"@type":"ListItem","position":2,"name":"%s","item":"%s"}]}]}'%(extra_schema,faq_schema(faqs),BASE,h1.replace('"',"'"),canonical)
    html=f"""<!DOCTYPE html><html lang="en-US"><head>
<meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<title>{title}</title>
<meta name="description" content="{desc}">
<link rel="canonical" href="{canonical}">
<meta name="geo.region" content="US"><meta name="robots" content="index,follow">
<meta property="og:title" content="{title}"><meta property="og:description" content="{desc}"><meta property="og:image" content="{BASE}/img/{gallery[0][0]}.webp"><meta property="og:type" content="website">
<link rel="preconnect" href="https://fonts.googleapis.com"><link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,500;0,600;1,500&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">
{PIXEL}
<style>{CSS}</style></head><body>
<nav><a class="logo" href="/" translate="no">GIUSEPPE&nbsp;BONELLI</a><a class="cta" href="#book">Book a session</a></nav>
<header class="hero"><div class="bg"><img src="/img/{gallery[0][0]}.webp" alt="{gallery[0][1]}"></div>
<div class="in"><div class="kick">{kick}</div><h1>{h1}</h1><p class="lead">{lead}</p><a class="btn" href="#book">Request a consultation</a></div></header>
<section class="wrap"><div class="eyebrow">The work</div><h2>Selected {kick_low} pieces</h2><div class="grid">{g}</div></section>
<section class="wrap" style="padding-top:0"><div class="info">{sec_html}</div></section>
<section class="wrap" style="padding-top:0"><div class="eyebrow">FAQ</div><h2>Good to know</h2><div class="faqs">{fa}</div></section>
<section class="wrap" id="book"><div class="formwrap">
<h2>{form_title}</h2><div class="s">Tell Giuseppe about your idea — he replies personally within 3–5 days.</div>
<form id="bf">
<input type="hidden" name="_source" value="{form_src}">
<div class="row two"><div><label>First name</label><input name="first" required></div><div><label>Last name</label><input name="last" required></div></div>
<div class="row two"><div><label>Email</label><input type="email" name="email" required></div><div><label>Phone / WhatsApp</label><input name="phone"></div></div>
<div class="row"><div><label>Your idea</label><textarea name="idea" placeholder="Style, subject, placement, size, timing…"></textarea></div></div>
<button class="btn" type="submit">Send my request</button>
<div class="note">By sending you agree to be contacted about your tattoo request. No spam.</div>
<div class="ok" id="ok">Thanks — your request has been sent. ✓</div>
</form></div></section>
<footer><div translate="no" style="font-family:'Cormorant Garamond',serif;letter-spacing:3px;color:#ece6da;font-size:18px">GIUSEPPE BONELLI</div>
<p style="margin-top:10px"><a href="https://www.instagram.com/giuseppe_gibi_bonelli/" target="_blank" rel="noopener">Instagram</a> · <a href="https://www.tattoodo.com/artists/peppebone" target="_blank" rel="noopener">Tattoodo</a> · <a href="mailto:info@giuseppebonellitattoo.art">info@giuseppebonellitattoo.art</a> · <a href="/">Home</a></p>
<p style="margin-top:8px;opacity:.55">© 2026 Giuseppe Bonelli. All rights reserved.</p></footer>
<script type="application/ld+json">{schema}</script>
<script>
var f=document.getElementById('bf');
f.addEventListener('submit',function(e){{e.preventDefault();var d=new FormData(f);d.append('_subject','New request — {form_src}');d.append('_template','table');d.append('_captcha','false');var b=f.querySelector('button');b.disabled=true;b.textContent='Sending…';
try{{fetch('/api/lead',{{method:'POST',headers:{{'Content-Type':'application/json'}},body:JSON.stringify({{first:f.first.value,last:f.last.value,email:f.email.value,phone:f.phone.value,source:'{form_src}',idea:f.idea.value,page:location.pathname}})}});}}catch(_){{}}
fetch('https://formsubmit.co/ajax/info@giuseppebonellitattoo.art',{{method:'POST',headers:{{'Accept':'application/json'}},body:d}}).then(function(r){{return r.json();}}).then(function(){{document.getElementById('ok').style.display='block';f.reset();b.textContent='Sent ✓';if(window.fbq&&FB_PIXEL_ID.indexOf('_')<0)fbq('track','Lead',{{content_name:'{form_src}'}});}}).catch(function(){{b.disabled=false;b.textContent='Send my request';window.location.href='mailto:info@giuseppebonellitattoo.art';}});
}});
function bx(o){{o.page=location.pathname;try{{navigator.sendBeacon('/api/track',new Blob([JSON.stringify(o)],{{type:'application/json'}}));}}catch(_){{try{{fetch('/api/track',{{method:'POST',headers:{{'Content-Type':'application/json'}},body:JSON.stringify(o),keepalive:true}});}}catch(e){{}}}}}}
bx({{event:'pageview'}});
var sd={{25:0,50:0,75:0,100:0}};
window.addEventListener('scroll',function(){{var h=document.documentElement,pct=(h.scrollTop+innerHeight)/h.scrollHeight*100;[25,50,75,100].forEach(function(p){{if(!sd[p]&&pct>=p){{sd[p]=1;bx({{event:'scroll',label:p+'%'}});}}}});}},{{passive:true}});
document.addEventListener('click',function(e){{var a=e.target.closest('a,button');if(!a)return;var t=(a.textContent||'').replace(/\\s+/g,' ').trim().slice(0,60);var href=a.getAttribute('href')||'';var ev=href.indexOf('mailto:')===0?'Email click':href.indexOf('tel:')===0?'Call click':'Click';bx({{event:ev,label:t||href}});}},true);
</script>
</body></html>"""
    d=os.path.join(DIST,slug);os.makedirs(d,exist_ok=True)
    open(os.path.join(d,"index.html"),"w").write(html)
    return canonical

COMMON_FAQ=[
 ("How much does a realism tattoo cost?","Pricing depends on size, placement and detail. Full-day realism sessions in the U.S. typically start around $1,200–$1,800; an exact quote follows once Giuseppe sees your idea and reference."),
 ("Do you require a deposit?","Yes — a non-refundable deposit confirms your appointment and is applied to the final cost. It's forfeited for no-shows or cancellations with less than 72 hours' notice."),
 ("How do I book?","Use the form on this page with your idea, placement and a reference image. Giuseppe reviews every request personally and replies within 3–5 days with available dates."),
]
PERSON='{"@type":"Person","@id":"%s/#giuseppe","name":"Giuseppe Bonelli","jobTitle":"Realistic Tattoo Artist","sameAs":["https://www.instagram.com/giuseppe_gibi_bonelli/","https://www.tattoodo.com/artists/peppebone"]}'%BASE

STYLES=[
 dict(slug="black-and-grey-realism-tattoo",h1="Black &amp; Grey Realism Tattoos",kick="Black &amp; Grey Realism",
   title="Black & Grey Realism Tattoos | Giuseppe Bonelli",
   desc="Hyper-realistic black & grey portrait, religious and wildlife tattoos by Giuseppe Bonelli — artist to Lautaro Martínez. Custom realism at the studio and on the 2026 U.S. tour.",
   lead="Photorealistic black &amp; grey tattoos — portraits, religious and sacred figures, statues and wildlife — built in deep contrast and fine gradient so they read like a photograph and hold their detail for years.",
   imgs=[("bg01","Black and grey realism portrait of Christ tattoo"),("bg06","Black and grey portrait realism sleeve"),("bg07","Black and grey realism chest portrait"),("bg03","Black and grey realism statue tattoo"),("co01","Black and grey realism portrait tattoo, warrior goddess"),("bg02","Black and grey realism saint portrait"),("bg05","Black and grey realism statue sleeve"),("bg08","Black and grey portrait realism tattoo")],
   sec=[("The approach","Giuseppe builds black & grey realism around a single light source, layering contrast so the piece stays readable as the skin softens over the years."),("Session length","Portraits usually need one full day; sleeves and back pieces are built across multiple sessions a few weeks apart."),("Pricing","Day-rate for large work, session minimum for smaller pieces. A non-refundable deposit secures your slot.")]),
 dict(slug="color-realism-tattoo",h1="Color Realism Tattoos",kick="Color Realism",
   title="Color Realism Tattoos | Giuseppe Bonelli",
   desc="Vivid color realism portraits and leg sleeves by Giuseppe Bonelli. Lifelike skin tones and saturation that last. Studio & 2026 U.S. convention tour.",
   lead="Vivid color realism — portraits, nature and bold color leg sleeves with lifelike skin tones, light and saturation, designed to stay rich for years.",
   imgs=[("p07","Color portrait realism tattoo, golden tears"),("p05","Color portrait realism tattoo"),("co02","Color realism owl tattoo"),("p09","Color realism character tattoo"),("co04","Color realism leg sleeve tattoo"),("co03","Color realism leg sleeve tattoo"),("co05","Color realism leg sleeve tattoo"),("p11","Full color realism sleeve tattoo")],
   sec=[("The approach","Color realism lives on accurate skin tones and clean saturation. Giuseppe layers color to read true in any light and resist fading."),("Session length","Color portraits typically need a full day; full color leg sleeves are staged across several sessions."),("Pricing","Day-rate for large color work, session minimum for smaller pieces; deposit confirms the booking.")]),
 dict(slug="wildlife-realism-tattoo",h1="Animal &amp; Wildlife Realism Tattoos",kick="Wildlife Realism",
   title="Animal & Wildlife Realism Tattoos | Giuseppe Bonelli",
   desc="Hyper-realistic lion, tiger, panther and eagle tattoos by Giuseppe Bonelli — including the lion on Lautaro Martínez. Studio & 2026 U.S. tour.",
   lead="Lions, tigers, panthers, eagles and serpents in hyper-realistic black &amp; grey — fur, scale and the catchlight in the eye, drawn by hand.",
   imgs=[("an01","Realistic black and grey lion tattoo"),("an04","Hyper-realistic tiger eye detail tattoo"),("an02","Realistic lion tattoo sleeve"),("an07","Realistic lion tattoo"),("an06","Realistic serpent tattoo"),("an05","Realistic eagle tattoo"),("an03","Realistic lion tattoo black and grey"),("champ02","Realistic lion back piece tattoo")],
   sec=[("The approach","Wildlife realism is won in the texture — every strand of fur and the wet catchlight of the eye. Giuseppe maps the animal to the body's anatomy."),("Session length","A single animal portrait is often one to two sessions; full wildlife sleeves are staged over weeks."),("Pricing","Day-rate for large pieces, session minimum for smaller; deposit secures the date.")]),
 dict(slug="sleeve-realism-tattoo",h1="Realism Sleeves &amp; Large-Scale Tattoos",kick="Sleeves &amp; Large-Scale",
   title="Realism Sleeves & Large-Scale Tattoos | Giuseppe Bonelli",
   desc="Full realism sleeves, back pieces and architectural realism (incl. the Milan Duomo) by Giuseppe Bonelli. Studio & 2026 U.S. convention tour.",
   lead="Full sleeves, back pieces and architectural realism — from cathedrals and the Milan Duomo to compositions that flow across the whole body.",
   imgs=[("sl02","Realistic statue full sleeve tattoo, front view"),("bg04","Realistic statue full sleeve tattoo, side view"),("bg03","Realistic statue full sleeve tattoo, inner view"),("sl01","Realistic warrior sleeve tattoo"),("sl05","Realistic Milan Duomo architecture sleeve"),("sl06","Realistic cathedral architecture tattoo"),("sl07","Realistic black and grey full sleeve"),("sl04","Large-scale realistic back piece")],
   sec=[("The approach","Large-scale realism is planned as one composition — flow, contrast and how it reads from across a room, not just up close."),("Session length","Sleeves and back pieces are built over multiple full-day sessions, spaced to let the skin heal between sittings."),("Pricing","Quoted as a project across sessions at a day-rate; a deposit confirms the first date.")]),
]
links=[]
for s in STYLES:
    es='{"@type":"Service","serviceType":"%s","provider":{"@id":"%s/#giuseppe"},"areaServed":"United States"},%s'%(s["kick"].replace("&amp;","&"),BASE,PERSON)
    sfaq=[("What does Giuseppe specialize in?","Giuseppe is a realism specialist — %s is one of his core styles, alongside black & grey, color, wildlife and large-scale realism. Every piece is custom, one-to-one."%s["kick"].replace("&amp;","&").lower())]+COMMON_FAQ
    links.append(page(s["slug"],s["title"],s["desc"],s["kick"],s["h1"],s["lead"],s["sec"],s["imgs"],sfaq,"Book a "+s["kick"].replace("&amp;","&").lower()+" piece","style:"+s["slug"],es))

CITY_IMGS=[("w01s","Realistic eye tattoo by Giuseppe Bonelli"),("an01","Realistic lion tattoo"),("bg01","Black and grey realism portrait"),("p07","Color portrait realism"),("sl05","Realistic architecture sleeve"),("an04","Realistic tiger eye"),("bg02","Black and grey realism saint portrait"),("champ01","Lautaro Martínez lion back tattoo")]
CITIES=[
 dict(slug="realism-tattoo-artist-portland",city="Portland",region="Oregon",dates="July 17–19, 2026",venue="Rose Quarter",event="Villain Arts Tattoo Festival",iso=("2026-07-17","2026-07-19"),verified=True),
 dict(slug="realism-tattoo-artist-new-hampshire",city="New Hampshire",region="NH",dates="July 24–26, 2026",venue="",event="Live Free or Die Tattoo Expo",iso=("2026-07-24","2026-07-26"),verified=True),
 dict(slug="realism-tattoo-artist-houston",city="Houston",region="Texas",dates="July 31 – August 2, 2026",venue="NRG Center",event="Villain Arts Tattoo Festival",iso=("2026-07-31","2026-08-02"),verified=True),
 dict(slug="realism-tattoo-artist-virginia-beach",city="Virginia Beach",region="Virginia",dates="August 7–9, 2026",venue="",event="Virginia Beach Tattoo Convention",iso=("2026-08-07","2026-08-09"),verified=True),
 dict(slug="realism-tattoo-artist-nashville",city="Nashville",region="Tennessee",dates="August 14–16, 2026",venue="The Fairgrounds Nashville",event="Villain Arts Tattoo Festival",iso=("2026-08-14","2026-08-16"),verified=True),
 dict(slug="realism-tattoo-artist-jacksonville",city="Jacksonville",region="Florida",dates="August 21–23, 2026",venue="",event="",iso=("2026-08-21","2026-08-23"),verified=False),
]
for c in CITIES:
    at=("at %s "%c["venue"]) if c["venue"] else ""
    lead=f"Looking for a realism tattoo artist in {c['city']}, {c['region']}? Giuseppe Bonelli — the Italian hyper-realism specialist whose black &amp; grey and color portrait work has been worn by footballers Lautaro Martínez, Gianluigi Donnarumma and Alessio Romagnoli — takes a limited number of bookings in {c['city']} during his 2026 U.S. convention tour (<b style='color:#ece6da;font-weight:400'>{c['dates']}</b>{(' · '+c['event']) if c['event'] else ''}). Booking is by appointment with a deposit; spots are limited."
    sec=[("What you can book","Black & grey realism, color realism, wildlife and portrait pieces sized to fit a convention session. Larger work can start in %s and continue at the studio."%c["city"]),
         ("Reserve early","Giuseppe takes a limited number of pre-booked clients per city. Send your idea now to secure a slot before the dates fill."),
         ("Worn by champions","His realism is worn by footballers Lautaro Martínez, Gianluigi Donnarumma and Alessio Romagnoli — now in %s."%c["city"])]
    faqs=[(f"Is Giuseppe Bonelli tattooing in {c['city']} in 2026?",f"Yes — Giuseppe is in {c['city']} on {c['dates']}{(' at the '+c['event']) if c['event'] else ''} as part of his 2026 U.S. realism tour. Reserve a slot through the form on this page."),]+COMMON_FAQ
    es='{"@type":"Person","@id":"%s/#giuseppe","name":"Giuseppe Bonelli","jobTitle":"Realistic Tattoo Artist","sameAs":["https://www.instagram.com/giuseppe_gibi_bonelli/","https://www.tattoodo.com/artists/peppebone"]}'%BASE
    if c["verified"]:
        locname=('"name":"%s",'%c["venue"]) if c["venue"] else ''
        loc='{"@type":"Place",%s"address":{"@type":"PostalAddress","addressLocality":"%s","addressRegion":"%s","addressCountry":"US"}}'%(locname,c["city"],c["region"])
        es+=',{"@type":"Event","name":"%s","startDate":"%s","endDate":"%s","eventStatus":"https://schema.org/EventScheduled","location":%s,"performer":{"@id":"%s/#giuseppe"},"url":"%s/%s/"}'%(c["event"]+(" — "+c["city"] if "Villain" in c["event"] else ""),c["iso"][0],c["iso"][1],loc,BASE,BASE,c["slug"])
    title=f"Realism Tattoo Artist in {c['city']} 2026 | Giuseppe Bonelli"
    desc=f"Giuseppe Bonelli — realism tattoo artist (Lautaro Martínez' lion) — is in {c['city']} on {c['dates']}. Black & grey & color realism. Reserve a convention slot."
    h1=f"Realism Tattoo Artist in {c['city']} — Giuseppe Bonelli"
    links.append(page(c["slug"],title,desc,f"{c['city']} · 2026 U.S. Tour",h1,lead,sec,CITY_IMGS,faqs,f"Reserve your {c['city']} slot","city:"+c["slug"],es))

# ---------- VILLAIN ARTS CIRCUIT PAGES (no fake dates/events: notify-me funnel) ----------
# Convention-weekend dates are public facts about the city's Villain Arts festival, shown as text only.
# NO Event schema here (Giuseppe's confirmed stops are only the summer tour above).
# LOCAL_NOTES: real, web-verified venue/neighborhood detail for select circuit cities (added a couple at a time
# so pages stop reading as identical templates). Verified 2026-07-12 via villainarts.com + local sources.
LOCAL_NOTES={
 "wildwood":("The venue & boardwalk","Villain Arts takes over the Wildwoods Convention Center at 4501 Boardwalk, right on the Wildwoods' two-mile boardwalk of classic Doo Wop motels and Morey's Piers. It's long-running — locals know it as the Wildwood Tattoo Beach Bash — and it sits in a town that already has a boardwalk tattoo scene (Love Rock Tattoo, Oxygen), so convention weekend runs alongside shops that tattoo year-round just blocks away."),
 "colorado-springs":("The venue & area","Villain Arts is held at the Norris Penrose Event Center on Lower Gold Camp Rd, in the foothills below Cheyenne Mountain and a short drive from the Broadmoor. It's a newer stop on the circuit — Colorado Springs' second year hosting the festival — pulling from the city's growing tattoo and outdoor-culture scene along the Pikes Peak corridor."),
}
CIRCUIT=[
 ("philadelphia","Philadelphia","Pennsylvania","January 23–25, 2026"),
 ("minneapolis","Minneapolis","Minnesota","January 9–11, 2026"),
 ("cleveland","Cleveland","Ohio","February 20–22, 2026"),
 ("san-diego","San Diego","California","February 13–15, 2026"),
 ("maine","Maine","ME","February 27 – March 1, 2026"),
 ("atlanta","Atlanta","Georgia","March 6–8, 2026"),
 ("charlotte","Charlotte","North Carolina","March 13–15, 2026"),
 ("chicago","Chicago","Illinois","March 20–22, 2026"),
 ("omaha","Omaha","Nebraska","March 27–29, 2026"),
 ("baltimore","Baltimore","Maryland","April 24–26, 2026"),
 ("kansas-city","Kansas City","Missouri","May 1–3, 2026"),
 ("cincinnati","Cincinnati","Ohio","May 8–10, 2026"),
 ("st-louis","St. Louis","Missouri","May 22–24, 2026"),
 ("palm-springs","Palm Springs","California","May 29–31, 2026"),
 ("denver","Denver","Colorado","June 5–7, 2026"),
 ("raleigh","Raleigh","North Carolina","June 12–14, 2026"),
 ("oklahoma-city","Oklahoma City","Oklahoma","June 19–21, 2026"),
 ("long-beach","Long Beach","California","July 10–12, 2026"),
 ("wildwood","Wildwood","New Jersey","August 7–9, 2026"),
 ("colorado-springs","Colorado Springs","Colorado","August 28–30, 2026"),
 ("meadowlands","Meadowlands","New Jersey","September 4–6, 2026"),
 ("asheville","Asheville","North Carolina","September 11–13, 2026"),
 ("syracuse","Syracuse","New York","September 18–20, 2026"),
 ("savannah","Savannah","Georgia","September 25–27, 2026"),
 ("milwaukee","Milwaukee","Wisconsin","October 9–11, 2026"),
 ("new-orleans","New Orleans","Louisiana","October 16–18, 2026"),
 ("san-antonio","San Antonio","Texas","November 13–15, 2026"),
 ("tampa","Tampa","Florida","November 20–22, 2026"),
]
for slug_c,city,region,when in CIRCUIT:
    slug=f"realism-tattoo-artist-{slug_c}"
    lead=(f"Looking for a realism tattoo artist in {city}, {region}? Giuseppe Bonelli — the Italian hyper-realism specialist whose black &amp; grey and color work is worn by footballers Lautaro Martínez, Gianluigi Donnarumma and Alessio Romagnoli — tours the U.S. tattoo-convention circuit year-round, including Villain Arts festival cities like {city} (convention weekend: <b style='color:#ece6da;font-weight:400'>{when}</b>). His confirmed Summer 2026 stops are Portland, New Hampshire, Houston, Virginia Beach, Nashville and Jacksonville — join the {city} list below and you'll be contacted first when a {city} date is confirmed.")
    third_block=LOCAL_NOTES.get(slug_c,("Worn by champions","His realism is worn by footballers Lautaro Martínez, Gianluigi Donnarumma and Alessio Romagnoli."))
    sec=[("Get on the "+city+" list","Send your idea now: when Giuseppe confirms a "+city+" date you're contacted first, before slots open publicly. Larger projects can also start at another tour stop."),
         ("What you can book","Black & grey realism, color realism, wildlife and portrait pieces sized for a convention session — every piece custom, one-to-one."),
         third_block]
    faqs=[(f"Is Giuseppe Bonelli tattooing in {city}?",f"Giuseppe tours U.S. tattoo conventions year-round. His confirmed Summer 2026 stops are Portland, New Hampshire, Houston, Virginia Beach, Nashville and Jacksonville; {city} dates are announced to the waiting list first — join it via the form on this page."),
          (f"When is the {city} tattoo convention?",f"{city}'s Villain Arts convention weekend is {when}. Giuseppe's own appearance dates are confirmed separately — join the list to be notified."),]+COMMON_FAQ
    title=f"Realism Tattoo Artist in {city} | Giuseppe Bonelli"
    desc=f"Giuseppe Bonelli — realism tattoo artist (Lautaro Martínez' lion) — tours the U.S. convention circuit. Join the {city} list for black & grey & color realism bookings."
    h1=f"Realism Tattoo Artist in {city} — Giuseppe Bonelli"
    links.append(page(slug,title,desc,f"{city} · U.S. circuit",h1,lead,sec,CITY_IMGS,faqs,f"Join the {city} list","circuit:"+slug_c,PERSON))

# ---------- HUB PAGE ----------
hub_cities=[("Portland, OR","realism-tattoo-artist-portland","Jul 17–19 · confirmed"),("New Hampshire","realism-tattoo-artist-new-hampshire","Jul 24–26 · confirmed"),("Houston, TX","realism-tattoo-artist-houston","Jul 31 – Aug 2 · confirmed"),("Virginia Beach, VA","realism-tattoo-artist-virginia-beach","Aug 7–9 · confirmed"),("Nashville, TN","realism-tattoo-artist-nashville","Aug 14–16 · confirmed"),("Jacksonville, FL","realism-tattoo-artist-jacksonville","Aug 21–23 · confirmed")]+[(c, f"realism-tattoo-artist-{s}", w) for s,c,r,w in CIRCUIT]
hub_links="\n".join(f'<a class="hc" href="/{u}/"><b>{n}</b><span>{w}</span></a>' for n,u,w in hub_cities)
hub=f"""<!DOCTYPE html><html lang="en-US"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>Realism Tattoo Artist Across the USA — Giuseppe Bonelli | Convention Circuit</title>
<meta name="description" content="Giuseppe Bonelli — Italian realism tattoo artist (Lautaro Martínez' lion) — tours tattoo conventions across the United States. Find your city and book black & grey or color realism.">
<link rel="canonical" href="{BASE}/us-tattoo-convention-circuit/">
<meta name="geo.region" content="US"><meta name="robots" content="index,follow">
<link rel="preconnect" href="https://fonts.googleapis.com"><link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,500;0,600;1,500&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">
{PIXEL}
<style>{CSS}
.hgrid{{display:grid;grid-template-columns:1fr;gap:10px;margin-top:30px}}
.hc{{border:1px solid rgba(201,162,75,.18);border-radius:8px;padding:16px 18px;background:#100d0a;text-decoration:none;display:flex;justify-content:space-between;align-items:center;gap:10px;transition:.3s}}
.hc:hover{{border-color:#c9a24b;transform:translateY(-2px)}}
.hc b{{font-family:'Cormorant Garamond',serif;font-size:19px;font-weight:600}}
.hc span{{font-size:11px;letter-spacing:1.5px;text-transform:uppercase;color:#c9a24b;white-space:nowrap}}
@media(min-width:820px){{.hgrid{{grid-template-columns:repeat(3,1fr)}}}}
</style></head><body>
<nav><a class="logo" href="/" translate="no">GIUSEPPE&nbsp;BONELLI</a><a class="cta" href="/#tour">Book a session</a></nav>
<header class="hero" style="min-height:60svh"><div class="bg"><img src="/img/w01s.webp" alt="Hyper-realistic eye tattoo by Giuseppe Bonelli"></div>
<div class="in"><div class="kick">U.S. convention circuit</div><h1>Realism, city by city.</h1><p class="lead">Giuseppe Bonelli — the Italian realism artist behind Lautaro Martínez' lion — tours tattoo conventions across America. Find your city, see the dates, and get on the list.</p></div></header>
<section class="wrap"><div class="eyebrow">Cities</div><h2>Where to find Giuseppe in the U.S.</h2><div class="hgrid">{hub_links}</div></section>
<footer><div translate="no" style="font-family:'Cormorant Garamond',serif;letter-spacing:3px;color:#ece6da;font-size:18px">GIUSEPPE BONELLI</div>
<p style="margin-top:10px"><a href="https://www.instagram.com/giuseppe_gibi_bonelli/" target="_blank" rel="noopener">Instagram</a> · <a href="mailto:info@giuseppebonellitattoo.art">info@giuseppebonellitattoo.art</a> · <a href="/">Home</a></p>
<p style="margin-top:8px;opacity:.55">© 2026 Giuseppe Bonelli. All rights reserved.</p></footer>
<script type="application/ld+json">{{"@context":"https://schema.org","@graph":[{PERSON},{{"@type":"BreadcrumbList","itemListElement":[{{"@type":"ListItem","position":1,"name":"Home","item":"{BASE}/"}},{{"@type":"ListItem","position":2,"name":"U.S. Convention Circuit","item":"{BASE}/us-tattoo-convention-circuit/"}}]}}]}}</script>
</body></html>"""
os.makedirs(os.path.join(DIST,"us-tattoo-convention-circuit"),exist_ok=True)
open(os.path.join(DIST,"us-tattoo-convention-circuit","index.html"),"w").write(hub)
links.append(BASE+"/us-tattoo-convention-circuit/")

import datetime as _dt
LASTMOD=os.environ.get("SEO_LASTMOD") or _dt.date.today().isoformat()
urls=[BASE+"/"]+links
sm='<?xml version="1.0" encoding="UTF-8"?>\n<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">\n'+ "".join('<url><loc>%s</loc><lastmod>%s</lastmod></url>\n'%(u,LASTMOD) for u in urls)+'</urlset>\n'
open(os.path.join(DIST,"sitemap.xml"),"w").write(sm)
open(os.path.join(DIST,"urls.txt"),"w").write("\n".join(urls)+"\n")
print("PAGES:",len(links))
