<template>
    <header class="header">
        <div class="header__logo">
            <a href="/"><img class="header__logo__img" src="../img/logo.png" alt="logo"></a>
        </div>
        <nav class="header__nav">
            <ul class="header__nav__list">
                <li class="header__nav__list__item">
                    <a class="header__nav__list__item__lk" href="/">Cats</a>
                </li>
                <li class="header__nav__list__item">
                    <a class="header__nav__list__item__lk" href="/">Forest</a>
                </li>
                <li class="header__nav__list__item">
                    <a class="header__nav__list__item__lk" href="/">Contact</a>
                </li>
                <li class="header__nav__list__item">
                    <a class="header__nav__list__item__lk" href="/">About</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default{

}
</script>

<style lang="scss">
.header {
    width: 90%;
    height: 100px;
    border: 1px solid purple;
    border-radius: 15px;
    background-color: rgba($color: purple, $alpha: 0.1);
    margin: 10px auto;

    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;

    &__logo {
        height: 100px;
        &__img {
            border: 3px dashed purple;
            border-radius: 47px;
            padding-top: 5px;
        }
    }

    &__nav {
        width: 50%; 
        &__list {
            display: flex;
            flex-direction: row;
            justify-content: space-around;
            list-style-type: none;

            &__item {
                &__lk {
                    text-decoration: none;
                    font-size: 30px;
                    color: black;
                    &:hover {
                        text-decoration: underline;
                    }
                }
            }
        }
    }

}
</style>