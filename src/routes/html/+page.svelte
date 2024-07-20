<div class="parent">
	<div class="header">шапка</div>

	<div class="users">
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
		<div>юзер</div>
	</div>

	<div class="chats">
		<div><a href="https://github.com/aksiere/test720">исходники здесь</a></div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
		<div>сообщение</div>
	</div>

	<div class="footer">подвал</div>
</div>

<style>
	.parent {
		height: 100%;

		display: grid;
		grid-template-columns: repeat(5, 1fr);
		grid-template-rows: 50px repeat(3, 1fr) 100px;
		grid-column-gap: 0px;
		grid-row-gap: 0px;
	}

	.header, .footer, .chats, .users {
		border: 1px solid black;
	}

	.header {
		grid-area: 1 / 1 / 2 / 6;
	}

	.users,
	.chats {
		overflow-y: scroll;
		padding: 1rem;

		& > div {
			margin-block: 2rem;
		}
	}

	.users {
		grid-area: 2 / 1 / 5 / 2;

		& > div:first-child {
			margin-top: 1rem;
		}

		& > div:last-child {
			margin-bottom: 1rem;
		}
	}

	.chats {
		grid-area: 2 / 2 / 5 / 6;
		display: flex;
		flex-direction: column-reverse;

		& > div:first-child {
			margin-bottom: 1rem;
		}

		& > div:last-child {
			margin-top: 1rem;
		}
	}

	.footer {
		grid-area: 5 / 1 / 6 / 6;
	}
</style>
