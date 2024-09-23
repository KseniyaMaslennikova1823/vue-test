<template>
    <footer class="footer">
        <div class="footer__block">
            <div class="footer__block__item">
                <h3>Cats</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas corrupti architecto quibusdam voluptatem sapiente eligendi beatae quo dignissimos magnam. Fuga quas atque dolorum corporis, ipsam numquam blanditiis expedita odio maiores!</p>
            </div>
            <div class="footer__block__item">
                <h3>Forest</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas corrupti architecto quibusdam voluptatem sapiente eligendi beatae quo dignissimos magnam. Fuga quas atque dolorum corporis, ipsam numquam blanditiis expedita odio maiores!</p>
            </div>
            <div class="footer__block__item">
                <h3>Contact</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas corrupti architecto quibusdam voluptatem sapiente eligendi beatae quo dignissimos magnam. Fuga quas atque dolorum corporis, ipsam numquam blanditiis expedita odio maiores!</p>
            </div>
            <div class="footer__block__item">
                <h3>About</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas corrupti architecto quibusdam voluptatem sapiente eligendi beatae quo dignissimos magnam. Fuga quas atque dolorum corporis, ipsam numquam blanditiis expedita odio maiores!</p>
            </div>
        </div>
    </footer>
</template>

<script>
export default{

}
</script>

<style lang="scss">
.footer {
    width: 90%;
    border: 1px solid purple;
    border-radius: 15px;
    background-color: rgba($color: purple, $alpha: 0.1);
    margin: 10px auto;

    display: flex;
    align-items: center;

    &__block {
        width: 100%;

        display: flex;
        justify-content: space-around;
        align-items: center;

        &__item {
            border-radius: 15px;
            background-color: rgba($color: #FFF, $alpha: 0.9);
            width: 20%;
            margin: 10px 0;

            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            padding: 10px;

            h3 {
                font-size: 30px;
            }
            p {
                font-size: 20px;
                margin-top: 15px;
            }
        }
    }
} 
</style>