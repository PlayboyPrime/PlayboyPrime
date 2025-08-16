<div align="center">
  <div>
    <img src="https://github.com/devicons/devicon/blob/master/icons/cplusplus/cplusplus-original.svg" width=55 height=55>
    <img src="https://github.com/devicons/devicon/blob/master/icons/csharp/csharp-original.svg" width=55 height=55>
    <img src="https://github.com/devicons/devicon/blob/master/icons/typescript/typescript-original.svg" width=55 height=55>
    <img src="https://github.com/devicons/devicon/blob/master/icons/javascript/javascript-original.svg" width=55 height=55>
    <img src="https://github.com/devicons/devicon/blob/master/icons/lua/lua-original.svg" width=55 height=55>
  <br>
  </div>
  <div>
    <img align="center" alt="GitHub Stats" src="https://github-readme-stats-navy-two-40.vercel.app/api?username=PlayboyPrime&theme=dark&show_icons=true&custom_title=Github%20Stats&hide_rank=true&include_all_commits=true&line_height=28" />
    <img align="center" alt="Top Languages" src="https://github-readme-stats-navy-two-40.vercel.app/api/top-langs?username=PlayboyPrime&theme=dark&show_icons=true&custom_title=Top%20Languages&layout=donut&line_height=28&exclude_repo=GTAV-Decompiled-Scripts" />
  </div>
</div>
<br>

# Main Projects

<details> 
  <summary>GTAV (Legacy & Enhanced) & RDR2 Mod Menu</summary>
  <ul>
    <li>Nebula (Previously called SuperBase)</li>
    <li>Mainly focused on GUI and backend. Does not have many features since it was first intended to be a public base</li>
  </ul>
  <li><img width="512" height="398" alt="image" src="https://github.com/user-attachments/assets/9d2065e7-d5c8-4ccd-8a43-64e37eb6c63b" /></li>
</details>

<details> 
  <summary>x64 Binary Obfuscator</summary>
  <ul>
    <li>Obfuscates x64 binaries to make reverse engineering harder</li>
  </ul>
  <h3>Original main</h3>
  <li><img width="833" height="745" alt="image" src="https://github.com/user-attachments/assets/09400633-20c1-4a85-8c6a-69cad7952da7" /></li>
  <h3>Obfuscated same function</h3>
  <li><img width="937" height="621" alt="image" src="https://github.com/user-attachments/assets/b5e646d7-a378-4fe0-98ff-e1de0110942a" /></li>
</details>

<details> 
  <summary>Dynamic Typed Script Langauge</summary>
  <ul>
    <li>SigmaScript (ignore the name please)</li>
    <li>Completly written from scratch. I wrote the Lexer, Parser, Compiler, VM, everything except for ImGui</li>
    <li>Dynamic typed script language intended for embedding which I discontinued to make a static typed language instead</li>
    <li>
      <details> 
        <summary>Embedding Functions</summary>
        <ul>
          <li><img width="780" height="165" alt="image" src="https://github.com/user-attachments/assets/658b319c-c0c1-43b8-8c8d-93ddac9d6745" /></li>
          <li><img width="852" height="632" alt="image" src="https://github.com/user-attachments/assets/22358654-d7fc-4aeb-9f36-4cbbb323c226" /></li>
        </ul>
      </details>
    </li>
    <li>
      <details> 
        <summary>Code & Disassembly</summary>
        <ul>
          <li><img width="639" height="93" alt="image" src="https://github.com/user-attachments/assets/2d037a22-ccd2-40d3-bc7c-9d8fd0218e06" /></li>
          <li><img width="920" height="648" alt="image" src="https://github.com/user-attachments/assets/f1f9f2bd-cf94-40ea-a426-34885eb8cdc8" /></li>
        </ul>
      </details>
    </li>
    <li>
      <details> 
        <summary>Experimental JIT Compiler</summary>
        <li>In case you dont know: JIT Compiler directly compiles to machine code instead of using a VM</li>
        <li>Code here was: return 123.f</li>
        <ul>
          <li><img width="417" height="537" alt="image" src="https://github.com/user-attachments/assets/bf56d658-95af-448e-b5be-f3c94adf9961" /></li>
        </ul>
      </details>
    </li>
  </ul>
</details>

<details> 
  <summary>Static Typed Langauge (unfinished)</summary>
  <ul>
    <li>NebulaScript</li>
    <li>Also completly written from scratch like SigmaScript</li>
    <li>Its still unfinished. Currenly it can compile variables and expressions</li>
    <li>It is mainly intended to be embedded</li>
    <li>This is the concept I wrote for it:</li>

- Break out of nested loops:
```cpp
while LoopName (true) {
	while (true) {
		break LoopName; // Break out of labeled loop
	}

	break; // Break out of current loop - Never reached in this example
}
```

- Default arguments for functions at any position:
```cpp
int example(int a, int b = 2, int c) {
	return a + b + c;
}

int example(1, , 3); // Second argument defaults to 2
```

- Multiple variables for if statements:
```cpp
if (int a, int b; func(&a, &b)) {
	...
}
```

- Functions with multiple return values (like lua & Python):
```cpp
int, int func() {
	return 1, 2;
}

int a, int b = func();
```

- New Loops:
```c
// while (true) style
loop {
	...
}

// do while style
loop {
	...
}
while (...)
```

- Only struct (no class) and inline private support:
```cpp
struct Example {
	int a;
	private int b;
private:
	int c;
public:
	int d;
};
```

- getter and setter:
```cpp
struct Example {
private:
	int a;
	public getter int a() {
		return a;
	};

public:
	int b;
	setter int b(int value) {
		b = value;
		return b;
	};
};
```

- goto, labels and inline assembly:
```cpp
s8 num = 0;

check_num:
if (num > 10)
	goto num_more_than_10;

asm {
	movi8 num, 10 // or implicit with movi num, 10
	jmp check_num
}

num_more_than_10:
...
```

### More:
- C++ like syntax
- Mainly focused on embedding
- Easily allow embedders to add variables and C++ functions that can be used and called from NebulaScript
- Pointer support
- Multithreading support
- JIT & VM Compilation
- Easy to understand compiler errors
  </ul>
</details>

<details> 
  <summary>Lua Protector</summary>
  <li>Made in only 5 hours</li>
  <li>Compiles lua files to luac and adds protections like:</li>
  <ul>
    <li>obfuscation: Obfuscates the script with stuff like string encoder, vm, compressor, function inliner, control flow obfuscation and more</li>
    <li>unluac crasher: Crashes unluac when attempting to unluac a protected script</li>
    <li>unluac time waster: Makes unluac take alot of time (~40min) just to crash at the end</li>
    <li>asm hider: Hides the assembly when attempting to disassemble the script (only shows the first few instructions)</li>
    <li>junk instructions: Adds junk instructions which do nothing but waste time when inspecting</li>
    <li><img width="750" height="246" alt="image" src="https://github.com/user-attachments/assets/e213960d-b5e2-46fa-9fdf-5316d2a72fab" /></li>
  </ul>
</details>

<details> 
  <summary>GTAV Injector</summary>
  <li>Legacy & Enhanced. Rockstar Launcher, Epic Games & Steam</li>
  <li>Repo: https://github.com/PlayboyPrime/GTAV-Injector</li>
  <ul>
    <li><img width="734" height="271" alt="image" src="https://github.com/user-attachments/assets/80538650-d839-4978-aaf8-77923f2f0a87" /></li>
  </ul>
</details>


# Old Projects

<details> 
  <summary>Discord Organizer Bot</summary>
  <li>Discord bot for selling custom discord bots with hosting time</li>
  <li>Fully automatic except for creating bot accounts because its against discord tos</li>
</details>

<details> 
  <summary>Discord System Bot</summary>
  <li>Customizable discord bot with many functions like:</li>
  <ul>
    <li>Admin Commands (Ban, Clear, Mute, Warn)</li>
    <li>Fun Commands (Meme, Mock)</li>
    <li>Utility Commands (Avatar, Calculate, Diff, Random, ServerInfo, Translate, UserInfo)</li>
    <li>Setup Commands (Setup systems listed below)</li>
    <li>Apply System (Forms)</li>
    <li>Join to Create System</li>
    <li>Welcomer & Leaver System</li>
    <li>Reaction Role System</li>
    <li>Roster System</li>
    <li>Guild Stats System</li>
    <li>Ticket System</li>
    <li>YouTube, Twitch & Twitter Notifier Systems</li>
    <li>Giveaway System</li>
  </ul>
</details>

<details> 
  <summary>Discord Global Chat Bot</summary>
  <li>Advanced global chat bot with many features like:</li>
  <ul>
    <li>Global Chat: Users can send text, images, stickers and emojis in a global channel which is then sent into every global channel of every guild. Text is checked for profanity which is then replaced with asterisk and Images, stickers and emojis are checked for nsfw which blocks the message</li>
    <li>Anti Spam: When a user sends too many messages in a short time or sends a guild invite it is blocked. If users in a guild send too many messages in a short time it was automatically reported</li>
    <li>Verify System: Users have to solve a captcha when sending a global message for the first time</li>
    <li>Reply System: Users could reply to other global messages which showed the replied to message in the global message</li>
    <li>Admin System: Admins can create giveaways (giveaway coins and profile customizations) and can see where global messages were sent from and can delete them in every global channel and can ban users from sending global messages</li>
    <li>Repot System: Users can report global messages with a modal to input a reason. The report is then sent into a channel where admins can take actions like Ignore, Delete and Ban</li>
    <li>Coin & Level System: Users get xp and coins by sending global messages</li>
    <li>Shop & Profile: All users have a profile which shows the user coins, level, xp, customizations and inventory. Customizations can be bought from the shop with coins</li>
    <ul>
      <li><img width="537" height="390" alt="image" src="https://github.com/user-attachments/assets/1c6a0730-5a36-459c-a5e4-e22c47ce2c82" /></li>
      <li><img width="467" height="402" alt="image" src="https://github.com/user-attachments/assets/a1552321-0acb-4851-a35d-3e5837d5511e" /></li>
    </ul>
  </ul>
</details>

<details> 
  <summary>Discord Modmail Bot</summary>
  <li>Simple modmail bot with good design and translations</li>
</details>
