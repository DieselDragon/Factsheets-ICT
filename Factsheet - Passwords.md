# Passwords

Passwords are a secret word (A bit like a door key) that you share with a service or website so that when you log-in to their services, they can be sure that it is you who is trying to log-in and not somebody else who knows your username or e-mail address. Passwords can be secure if they are used and safeguarded properly, but choosing and managing passwords can also be a massive headache for people because of the rules that often need to be followed and the fact that people tend to forget them if they don't use them often enough.

To add to this; Even though it is very tempting, the same password should NEVER be used across multiple sites or services. If the database of one website is leaked (Stolen) the thieves who stole it will try to use your e-mail and password on other sites in the hope of accessing and stealing your accounts on those sites too.

This factsheet explains some of the issues with passwords, how they can be hacked, mistakes to be avoided, and techniques that can help you to create - And remember - A unique and hard-to-hack password for every website that you use.


## Password problems:
A password is like your house key - It lets you (And only you) into your house, even though your family, friends and others who know your (e-mail) address can still come to your front door and knock if they want to visit you. Unlike house keys - Which can be found again and used if lost - Passwords are keys that are memorised and can be lost forever when you forget them, which is very easy to do when considering your "Mental keyring" could have well over 100 passwords in it.
Although you could use the same key (Password) for every door (Website) you need to open, this is a very bad practice - Some banks and financial services will consider this a breach of their terms and refuse protection from theft if you do - Because if a website is hacked and your e-mail/password is stolen, those hackers will try your details on other sites to see if they can hijack (Steal) your accounts on those too. This is how a number of Facebook accounts got hacked shortly after a breach of the LinkedIn user database - Many people were using the same e-mail and password for both sites.

One of the main problems with passwords (And another reason not to use the same one across every website) is that you have to enter them into the website every time you sign-in to your account, and each sign-in attempt is a potential window for password theft. If a website was hacked to send every password entered to an unauthorised third party as well as the site you wanted to access (This has been done many times via an attack called "Cross-site scripting") that unauthorised party would receive a copy of every user name/e-mail address and password, and they could use this to try to access your accounts on other sites.
To apply the house key analogy: It would be like having an invisible Mr Minit sat in front of your door who copies every key that is put into the lock, who can then use those copies to enter your house whenever they like. If you used the same key for your house, workplace and car, then the one copied key - Stolen only once - Would give them access to all three instantly!

In short: A password is a key that is as secure as you keep it...And though having 150 keys on a keyring is far less convenient than just having one or two, 150 separate keys is a lot more secure than one or two "Master" keys that could allow access to lots of your stuff if they were stolen.
Remember: Security and convenience are opposing ends of the same scale...And though convenience is always easier, taking the time and effort to stay toward the security end of the scale is a worthwhile investment in making your passwords harder to hack and less damaging when* they get hacked.
(* - Make no mistake - This WILL happen to you at some stage. Many sites don't have the high level of security you might expect, and even the best security can be compromised if the wrong people are in the wrong places.)


## How passwords are Hacked:
Many websites will claim that their user databases are "Encrypted to FIPS-140 compliant standards" or "100% secure" (This is actually impossible) and in many cases this is true, but any database that has to be online to do it's job (Like checking log-on requests) is potentially vulnerable to theft - Whether this be because a copy of the database was put in a publicly accessible location by accident, a copy of the database was on a disk the company didn't erase before throwing it away, or is the result of an "Inside job" by a disgruntled employee or undercover hacker. It only takes one copy of the database for it to fall into the wrong hands (Because more copies can be made without the companys awareness) and it could be many months or years before the theft of a database is discovered and users are warned about it.

Passwords are normally stored using non-reversible one-way algorithms (Message digest algorithms; SHA-256 and SHA-512 being the most common, MD5 and SHA-1 are no longer regarded secure) and when you log-on to a site the password you provide is "hashed" using the same algorithm and compared with the hashed copy of your password in the database - If the hashes match, you've provided the right password and you're let into your account. If the hashes don't match, then you've provided the wrong password - The website tells you this, and asks you to try again.

Although the algorithm can't be run backwards - i.e. It's not possible to put a hash in one end and get the password out of the other - It IS possible for a hacker to take a long list of hashes and perform a "Dictionary Attack" where words from a dictionary file (Usually the dictionaries of all global languages, plus popular nouns like "Paris" or "Obama" and other names) are hashed with the same algorithm in turn and those hashes compared with those from a user database - If hashes in the database match the one for the word that was just hashed (See below) the Hacker knows that those accounts used that word as their password.

Worked example: My password is "Login" and is hashed with SHA-1, so my database entry is "User: somebody@example.com, Password: 4e5a2893bdcc7d239c1db72e4c4ffbe4bea73174". While running a dictionary attack the Hacker hashes the word "Login" and gets the same result, and from this she knows that any user whose password is "4e5a2893bdcc7d239c1db72e4c4ffbe4bea73174" has used "Login" as their password. After doing this with all 7,500,000+ words in her dictionary (Which doesn't take long) she has successfully recovered the passwords for more than 50% of the accounts in the database that she'd stolen, and until she tries to abuse that information (By trying to steal or sell accounts) no-one will know she has done this or that she has a list of compromised logins at her disposal.

Because the majority of password hacks rely on users choosing simple dictionary words for their passwords - And the algorithms used change the output significantly if even one letter is changed ("Login" is 4e5a2893bdcc7d239c1db72e4c4ffbe4bea73174, but "Log!n" is 2b0ad6c7ecdf2f2137290893ac83882a02e6c393 and "7oG1n" is 2d88ac08e07a81f0ebd3b8dc1955e1f718133d28) - Dictionary attacks can be made more difficult by choosing words that won't appear in dictionaries (Or lists of names, cities, football clubs etc), made-up words that are complete nonsense, using special characters or symbols in place of letters and/or between words, and ideally a combination of all three.

Finally: Many password hacking tools have the capability to try numbers, special characters and symbols in place of letters in common words, so using garbage words (8+ letter words made up by bashing the keyboard randomly), delimiters of 2+ special characters, and letters from extended alphabets (e.g. Accented characters from the Spanish alphabet) is much better if you have a non-English keyboard or otherwise know how to input them reliably. Because of their prominence on English keyboards the symbols !?@#$£%^&.+-*/=,(){}[]<>_:;|\ will always be included in more advanced dictionary attacks, so characters like «¡¿ß₨€₪» should be strongly considered if you can use them.

**CAUTION:** Keyboards and the characters on them differ vastly around the World as does the position and input method of common symbols, so consider this carefully if you may need to access your accounts from computers with French, Japanese or Spanish keyboards, where symbols like £ and $ might not be readily available, or difficult to input if they are.


## Mistakes to avoid when choosing and using passwords:
A lot of this section boils down to basic common-sense, and the reasoning behind much of the following can be found by referring to the previous section. In particular...

  × NEVER give your password(s) - Or any one-time SMS/app codes - To anybody for any reason, not even friends/relatives/partners, representatives of a reputable company, or the Police. None of the latter will ever ask you for passwords, and any claim otherwise comes from somebody attempting fraud.
  
    ➥ Genuine representatives of companies like Amazon will never call and ask you to "verify" a purchase and/or give your password. Genuine company representatives can access your account directly without the password through the company's own systems, and will usually request personal details or ask you to correctly answer questions about recent purchases to verify that you are the account holder.
    
    ➥ If you are cold-called by a bank/credit card or company asking to "Verify" a purchase or telling you there's been "Suspicious activity" on your account; Hang-up immediately, especially if the call sounds automated. Most online companies do not call if you havn't specifically asked them to (They usually e-mail) and the safest way to see if you need to "Verify" anything is to log-in to that site directly - Anything of issue will be bought to your attention when you log-in.
    
    ➥ The Police - Who would need a warrant to access your accounts - Have an established legal process to follow, and cannot command this of you without due cause. You have the right to seek legal counsel before releasing your password(s) to the Police, and this would be highly advisable.
    
  × NEVER write your passwords down in a complete and obvious form, and especially not alongside the usernames/e-mail addresses they relate to.
  
  × NEVER click links in e-mails/SMS messages, and never log-in using forms sent by e-mail - Go to the site directly and log-in ONLY via their sign-in page. This applies even if an e-mail/SMS claims that action is "Urgent" or "Your account may be suspended". (If either are claimed, the e-mail/SMS is fake.)
  
  × NEVER use "Remember me" or "Save my password" features on any computer/device that is shared with other people. This is especially important with public (Library) computers and devices.
  
  × Never use any password manager that hasn't earned a strong reputation and the recommendation of recognised, trusted security experts and organisations.
  
    ➥ Password managers are a very security-critical application, many criminals have created fake ones that they use to capture and steal passwords and logins, and using "free" ones found on app stores is an extremely unwise practice.

  × Don't use directly obvious or "Top 100" passwords i.e. Password, qwerty, VoteRemain, LeaveEU, OpenSesame, asdf, LetMeIn, 1234, qwertyuiop, password123, GodSaveTheQueen and others.
  
    ➥ To safely check if your password is a "Top 100", search for a list of top 100 passwords and use the "Find on page" feature in your browser to search for the first three letters ONLY of your intended password. This will show you if any starting with the same three letters exist without exposing your intended password in full.
    
  × Don't use passwords that are an individual word, name, or common phrase in any culture or language. Avoid things like VivaEspana, ManchesterUnited, GodBlessAmerica, RealMadrid, ViveLeFrance, PSVEindhoven, FroheWeinacht, MuchoGracias etc etc.
  
  × Don't write your passwords down in such a way that others could steal, read, understand and use them.
  
    ➥ See the later section "Recording your passwords in a secure manner" for safer alternatives.
    
  × Don't use "Remember me" or "Save my password" features on shared computers/devices.
  
    ➥ If using this feature on a device you intend to sell/give away make sure you remove ALL stored usernames, accounts and passwords before doing so.
    
  × Don't trust your accounts to password managers (Like KeyPass or those built-in to your web browser) UNLESS you know exactly how to back-up and safeguard the master files correctly. Though password managers generate much stronger passwords than humans, any failure or loss of the password manager application (Or your master password) will lock you out of all of your accounts at once.


## Tips for choosing Strong, Secure, and Hard-to-Hack passwords:
  ✓ Use randomly selected subjects (Selection topics) as a source of base passwords, ideally from a pool of several wide and diverse topics.
  
  ✓ Avoid passwords/selection topics that relate in any way to things which you are overtly associated. If you are known to be a keen car enthusiast, a targeted attack might try car, modification and sound system brands to "Zero in" on your passwords.
  
  ✓ Choose password selection topics from hobbies and interests that you have no dislike of but no known interest in e.g. Stamp collecting, Football, Morris Dancing etc.
  
  ✓ Expanding your pool to cover topics from other cultures and languages may further increase password security.
  
  ✓ Choose passwords from every language that you speak, if possible. One of the simplest techniques may be to avoid the use of English.
  
    ➥ If you speak a minority or regional language (Cymraeg, Gaeldheg, Kernow etc) make use of it; These languages are likely to be much stronger against dictionary attacks compared with English, French or Spanish.

  ✓ Try to choose a password of 12 characters or more (Ideally, the longest the site will accept).
  
  ✓ Use a mix of upper and lower case letters, numbers, punctuation and symbols - The more complex and less "Dictionary like", the better.
  
  ✓ Use of non-English characters (ÅÆÇÑÜß etc) may increase password security by avoiding dictionary attacks targeting English-speaking users.
  
  ✓ Similarly; Use Emoji in your password, if the website will allow it.
  
  ✓ Take care to ensure you can reliably choose and input the correct (identical) emoji or non-English characters on different platforms/devices, and apply caution with variant emoji (e.g. male/female/neutral of any ethnicity) as you will need to use that exact emoji/character every time. 
  
  ✓ Include pre-chosen garbage sequences in varying measure as suggested in a following section.
  
  ✓ Never write passwords down - Instead, write "hints" to your password that only you will understand and be able to use.
  
    ➥ See the third method in the next section.

  ✓ If a website lets you choose a logon or user name for account access rather than your e-mail address, use that feature. Choose a username that is different from those you use in other places where you can, except perhaps where you want people to be able to identify you across different services.
  
     ➥ For confidential or sensitive accounts, choose usernames that appear to be nonsense or are completely meaningless. A randomised username like "kwjqwejiwkdwdcfw" (Take care to note it down carefully) is far more secure for online banking than the username by which you are publicly known on social media.
     
     ➥ Be cautious with some online banking systems which issue a user ID that contains all or part of your date of birth, and which the user cannot change by themselves - For anyone who knows your DoB (Which you might've made public on social media) finding your username will be very easy. If you are with a bank that uses this system (Like NatWest) ask them if you can have a different user ID which does not include your DoB or account information at all.
     
  ✓ If you are a power user with access to a personal domain and can route all domain e-mail to your personal inbox, use separate e-mail addresses for each website. This will break the association between usernames/e-mail addresses that dictionary attacks rely on (MyBank@example.com won't match their hacked password for Facebook@example.com) and will increase per-account security considerably.
  
     ➥ For sensitive or confidential accounts; Using an e-mail address that resembles a randomised string (e.g. BiwhfdOjdheiuE@example.com rather than BankOfEngland@example.com) may increase account security and lead to early awareness of a breach if spoof e-mails start to be received at that address.

  ✓ As an extra layer of security: If the website or service offers two-factor authentication (Using SMS messages or a smartphone app) always enable this if you are able to make use of it, and especially so if you normally access your account via public computers. This adds an extra step to logging-in that requires you to verify your login via your phone (By responding to a notification, or inputting a code received by SMS) and ensures that even if someone manages to learn your password they will still need access to your phone to access your account. The notifications can also be a valuable early warning if somebody tries to hack into your account, given you would only expect to receive them if you were trying to log yourself in at that moment.


## How to create strong passwords...And remember them:
There are probably as many methods for generating, remembering and retrieving passwords as there are human beings on our planet (Remember: Passwords and cryptography predate computers by hundreds of years!) but three that come recommended by trusted organisations include:

**✓ GCHQ recommendation: Pass-phrases.**

Phrases and sequences of words that describe something relatable tend to be easier to remember than single words made up of a mash of letters, numbers and special characters, and GCHQ recommend choosing a phrase that describes something you can easily relate to - Such as a memorable seaside holiday - And build a phrase on that, such as "ILovedMyWeekInBlackpool". This can be used by itself, though transforming this in some way - Like changing every third consonant into it's visually closest number (Producing "ILove9My7eekIn8lac4pool") or reversing the order of vowels (Producing "OLovadMyWiekEnBleckpoil" - Will increase security considerably.

**✓ NCSC recommendation: Three word descriptions.**

In a similar vein to GCHQ, the NCSC recommends thinking of something that you know - Such as a favourite person or object - And then choosing three words to describe them. If you were thinking of your mother for example, your three chosen words might be "Tea, Lovely, Short". These can be used together to make a password on their own (Consider mixing up the word order across sites) and again, transforming vowels and consonants using a transformation rule of your own choosing (Which should be kept confidential) also comes recommended.

**✓ My method: Three-factor authentication.**

Some of the strongest authentication systems combine something you know (A password or PIN) with something you have (A phone, security key or smartcard) to reduce the possibility of unauthorised access; You don't just have to steal the password/PIN (Which can be done remotely) but also a physical object. Although it's not possible to replicate this on password-only systems, it is possible to use the same approach to generate widely variable passwords where access to both the account holders knowledge and physical objects are necessary to gain access to that password.

Central to this is the use of a code table - This is simply a list of randomly generated text strings (sequences) which are used to form parts of passwords. These are combined with parts of passwords that have been committed to memory (NEVER written down) and are stored as non-obvious clues in a password journal. The process works a bit like this:

  1. My memorised passwords are: Lorum Ipsum Dolor Sit Amet. Password 2 would be "Ipsum".

       ➥ These are strictly memorised and are NEVER written down anywhere. (Except, perhaps, in a sealed envelope filed alongside your Will for the use of your Executor, who may need to be able to access your accounts in pursuit of their duties when that time comes.)

  2. My randomised codes are: ij*vd io!qm dl&kw md$sq. Code 3 would be "dl&kw".

       ➥ These are stored in a safe but easily reachable place such as a purse or wallet, and another copy kept somewhere safe for backup purposes. These can be stored in/with the password log if preferred, but storing them separately will increase security further.

  3. I need a new password for a website, and roll a dice three times to get the numbers 2, 3, and 1.

  4. This randomly selects a password formed of Code 2, Password 3, and Code 1 (In that order) producing the password "io!qmDolorij*vd".

       ➥ The selection order could also be reversed to yield "Ipsumdl&kwLorum", or randomised every time if you prefer. More dice rolls (Say; 4, 5 or even 6) will produce stronger passwords.

  5. Once generated, the construction of the password and a clue to which website it's used with is noted in the password journal in a manner that is personal (And ideally only comprehensible) to the user, allowing them to recreate that same password reliably at any point in the future.

       ➥ This could be done as drawing the dice rolled - Using one colour for the password dice and another for the code dice to differentiate them - Or by coming up with a different and personal way of recording the construction "Code 2, Password 3, Code 1". The more personal to the user and incomprehensible to the casual observer (e.g. By using codes/symbols or terminology known only in the users profession) the better.

  6. So long as each password generated uses at least one of the memorised passwords - And so long as those passwords remain confidential to the user (i.e. NEVER written down!) - Correct generation of any password from the information in the password journal will always require the users awareness and input, even if another person accesses and is able to comprehend the password journal.

       ➥ The use of strictly memorised elements means that even with the code table to hand the password journal is rendered entirely useless to unauthorised persons, whilst reducing the burden of memory on the user to a handful of personally chosen words/phrases which can be memorised, spelt and punctuated entirely in the manner of the users choosing.

This makes reconstruction of previously chosen but not-often-used passwords a much more straightforward yet mostly secure process in that it permits recording of how the password is constructed whilst omitting critical information, ensuring that only the user themselves is able to combine the information between the three to obtain the full password. This of course assumes the user has chosen memorised passwords that cannot easily be guessed by a person who knows them well (Deliberate misspellings may be advisable, especially for those with a reputation for good grammar) and which have a strong possibility of remaining permanently secret.

Finally: If you can, come up with a system for changing the memorised passwords if ever you need to - Such as if you were obliged by a court to provide them to the Police. Although wholly memorised passwords are very safe as a rule, they should be regarded very much like "Master Keys" and any exposure of them to other parties should be avoided at all costs.


## Recording your passwords in a secure manner:
As noted above, the very worst thing you can do is to record your passwords in an understandable way that other people can read and abuse if they ever get access to your password log, so dividing the password information up between 1-3 physical records (Notebooks etc) and your brain will considerably increase the security of your accounts and the passwords which protect them. Some tips that may help you achieve this might be:

  ✓ NEVER write down a password in a clear and obvious form, and definitely not with its username or e-mail address. Instead, write a "Hint" or "Clue" that you will be able to understand (Considering that you may need to use it years later, so use methods that you are likely to remember long-term) but which will be unreadable or confusing to others.
  
  ✓ If you have close knowledge of an industry where unusual codes or symbols are used, consider hints based around those schemes.
  
     ➥ An electrician might choose methods based on symbols from BS:3737, a chemist might choose the formulae of certain drugs, and a train driver might choose schemes based on signalling rules, for example.
     
  ✓ Similarly: If you speak languages other than English (Particularly localised languages, like Cornish) consider using those languages rather than English. Remember though that many major languages have wide global fluency (UK/USA has many French and Spanish speakers too) and this should only be applied as an extra obstacle to a potential password thief, NEVER as the sole means of protection.
  
  ✓ If you are able to, store username information and their associated password hints in separate places - A book of password clues without usernames (Or vice-versa) will force an adversary to find out the missing info for themselves or spend more time searching for the opposite record, which means much more work for them and will greatly reduce opportunist theft.
  
  ✓ Consider separating functional parts of password reminders across different pages or chapters to make them hard to steal using a camera.
  
  ✓ Be very careful when storing password reminders on electronic devices, particularly on PCs/smartphones or any device with connectivity to the Internet.
  
     ➥ Ideally, at least some of the information should be written down by hand. Handwritten notes are a lot more secure than iNote.

  ✓ Finally: Once you have found a method that works well for you, make it a part of your daily life. The more you use it the more instinctive it will become, and after a short time you'll find that you're able to store and recall passwords securely yet reliably in a manner that only you are able to understand.
  
     ➥ If you manage to devise a method where people would not be able to identify and access/compromise your accounts even if all of the written information (Password and Username journals, code charts etc) had been posted in public, then you almost certainly rank amongst the top 20% of most secure users and the likelyhood of falling victim to most attacks is considerably reduced. This is a good place to be, but take great care NOT to become complacant because of it!

  ✓ Remember: Good security requires constant hard work, and invasion of ones security requires only one mistake. The greater the caution and the smaller your attack surface, the less likely you are to be hurt when somebody hacks you.
  
     ➥ And remember: You WILL be hacked at some point. Even the strongest level of security can be compromised ("100% secure" is 100% impossible) so taking measures from the start to minimise the impact of any damage is equally as important as keeping the hackers out!


**WiP:** *Hand inserted 2021-05-22 as a quick get-me-up. Later versions will be created offline and this file will be updated as appropriate.*
