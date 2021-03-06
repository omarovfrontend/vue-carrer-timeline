<template>
    <div>
        <header class="header">
            <h1 class="header__title">{{ name }}</h1>
            <p class="header__description">
                I’m a web UI designer / fron-end developer, a problem solver who always <br>
                loves a challenge and enjoys working on precise &amp; detailed projects.
            </p>
        </header>

        <div class="contacts">
            <ul class="contact-list">
                <li class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <a class="contact-item__link" href="mailto:karim@karimtarek.com">{{ email }}</a>
                </li>
                <li class="contact-item">
                    <i class="fas fa-phone"></i>
                    <a class="contact-item__link" href="tel:+15140000000">{{ phone }}</a>
                </li>
                <li class="contact-item">
                    <i class="fas fa-globe-europe"></i>
                    <a class="contact-item__link" href="#">{{ url }}</a>
                </li>
                <li class="contact-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <span class="contact-item__link">{{ location }}</span>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'theHeader',

        data() {
            return {
                name: 'Omarov Shamil',
                email: 'karim@karimtarek.com',
                phone: '+1 514 000 0000',
                url: 'www.karimtarek.com',
                location: 'Montreal, Canada',
            }
        }
    }
</script>

<style lang="scss" scoped>
    .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-bottom: 10px solid #e74c3c;
        padding-top: 30px;
        padding-bottom: 10px;
        color: #34495e;

        &__title {
            font-family: 'Roboto Slab', serif;
            font-size: 30px;
            font-weight: 100;
        }

        &__description {
            font-size: 9px;
            line-height: 12px;
        }
    }

    .contact-item {
        &__link {
            padding-left: 3px;
        }
    }
</style>