# Git Tools

A set of useful shortcuts for _Git_ commands.

## Tools

<details>
	<summary><code>git work</code></summary>
	<ul>
		<li>A simple alias of <code>git checkout</code>.</li>
	</ul>
</details>

<details>
	<summary><code>git loglist</code></summary>
	<ul>
		<li>Returns a simple, compact list of all commits. It's an alias.</li>
	</ul>
</details>

<details>
	<summary><code>git save</code></summary>
	<ul>
		<li>Allows to execute <code>git add -A</code>, <code>git commit</code>, <code>git push</code>, and <code>git log -1</code>, all at once. It is a bash function.</li>
		<li>
			<b>Usage:</b>
			<ul>
				<li><code>git save</code>
					<ul>
						<li><code>--skip-add</code> or <code>-s</code>:</li>
						<li>Skips <code>git add -A</code>.</li>
						<li>The default is to not skip.</li>
						<li><code>--amend</code> or <code>-a</code>:</li>
						<li>Apply <code>--amend</code> on the <code>commit</code>.</li>
						<li>If <code>--push</code> is also used, then it also applies <code>-f</code>.</li>
						<li><code>--reamend</code> or <code>r</code>:</li>
						<li>Apply <code>--amend --no-edit</code> on the <code>commit</code>.</li>
						<li>If <code>--push</code> is also used, then it also applies <code>-f</code>.</li>
						<li><code>--push</code> or <code>-p</code>:</li>
						<li>Executes <code>git push</code>.</li>
						<li>The default is to not execute.</li>
						<li><code>"title"</code>:</li>
						<li>The "commit title", applied with <code>-m</code>.</li>
						<li><code>"message"</code>:</li>
						<li>The "commit message", applied with <code>-m</code>.</li>
					</ul>
				</li>
			</ul>
			<ul>
				<li>The first <code>"text"</code> is the <code>"title"</code>, the second is <code>"message"</code>. All the following <code>"text"</code> is ignored.</li>
				<li>The order of the params doesn't matter.</li>
				<li>If <code>--amend</code> is used with <code>--reamend</code>, then <code>--reamend</code> is applied.</li>
				<li>If <code>--reamend</code> is used with <code>"title"</code>, then <code>--amend</code> is applied.</li>
				<li>The shorthands can be used together. Ex.: <code>-ap</code> applies both <code>--amend</code> and <code>--push</code>.</li>
				<li>It is necessary to have a <code>"title"</code>, or an error is thrown. Except when <code>--reamend</code> is used.</li>
			</ul>
			<li>
				<b>Examples</b>:
				<ul>
					<li><code>git save --amend --push "Titulo" "Mensagem"</code>.</li>
					<li><code>git save -sa "Titulo" "Mensagem" -p"</code>.</li>
					<li><code>git save "Titulo" -p "Mensagem" --amend</code>.</li>
					<li><code>git save -r"</code>.</li>
					<li><code>git save -rps"</code>.</li>
				</ul>
			</li>
		</li>
	</ul>
</details>

<details>
	<summary><code>git quicksave</code></summary>
	<ul>
		<li>Simply executes <code>git save</code> with the current date(<i>DD/MM/AAAA</i>) as <code>"title"</code>.</li>
	</ul>
</details>

## Installation
It's the file `C:\Users\YOUR_USERNAME\.gitconfig`, present if _Git_ is installed.
