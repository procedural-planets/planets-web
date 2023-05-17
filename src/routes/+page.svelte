<script lang="ts">
	import '../reset.css'
    import JournalEntry from '../components/JournalEntry.svelte';
</script>

<main>
    
    <div class="title">
        <h1>Procedural Planets</h1>
        <p>by Albin Kempe, André Fredriksen & Vilhelm Hellmér</p>
    </div>
    <div class="jorunal">
        <JournalEntry
        entry_title = "Making Our Own Filter! (Really Cool)"
        entry_date = "2023-05-17"
        entry_image =  {{
            src: "4.png",
            id: "4",
            text: ":)",
            desc: "Procedurally generated planet"
            }}
        entry_text = "Yepp that's it!
        "
        />
        <!------------------------------------------------------------->
        <JournalEntry
        entry_title = "Planet X?"
        entry_date = "2023-05-16"
        entry_image =  {{
            src: "3.png",
            id: "3",
            text: "Procedurally generated planet with a simple shader.",
            desc: "Procedurally generated planet"
            }}
        entry_text = "Ahh, an exquisite piece of planetary marvel! Since last time, we have implemented a new type of noise filter and added a simple shader to our planet. 
        
        ...
        "
        />
        <!------------------------------------------------------------->
        <JournalEntry
        entry_title = "Make Some Noise!"
        entry_date = "2023-05-14"
        entry_image =  {{
            src: "2.png",
            id: "2",
            text: "Procedurally generated planet using layerd simplex noise.",
            desc: "Procedurally generated planet"
         }}
        entry_text = "To change the shape of our sphere to make it into a planet, noise is used to determine the elevation of points on our sphere. The modified version of simplex noise by Sebastian Lague is used in our implementation. Our plan for the future is to implement different types of noise. We have not yet settled on which one, but we have mentioned Worley noise during our group meetings. At this point, we are just following along Lague's tutorial.

        Using a single layer of simplex noise alone to determine the elevation of points on our sphere basically create a blob. We have different parameters that change the characteristics of the terrain such as rougness and strength. Turning up the roughness increases the distance between points which turns the planet into a spike ball. Pretty cool. At this point we can create blobs, spike balls and kinda meteorites - but that's not really what we are here for. We want that planet shape!!

        To turn our blob into a planet the only thing we need to add is a minimum elevation value to our code. This will ensure that no points have a lower elevation than the minimum elevation. With the right settings, the points that are set to this minimum value will create the oceans on our planet and other points will create chunks of land. This can clearly be seens in the image above. We have our planet! Project finished? No.

        One blob high-lone cannot maketh a planet, but two c'rtainly can. That's right Shakespeare! One blob cannot be both farmland and mountains, it can only be one of them. To achieve an authentic look on our planet, we need to layer our noise. This only means creating multiple noise layers. When we want to calculate the elevation of a point, the output from each noise layer is added to the point's elevation.

        Mountains sticking out of the ocean is ruining the immersion. We only want mountains to appear on land! To fix this, we use one of the noise layers as a mask for the other layers. After doing this, we achieve the result in the image above! Done and dusted for this time!
        "
        />
        <!------------------------------------------------------------->
        <JournalEntry
        entry_title = "A Sphere Is Born"
        entry_date = "2023-05-12"
        entry_image =  {{
            src: "1.png",
            id: "1",
            text: "A basic sphere. Note the lines indicating different surface normals.",
            desc: "sphere"
         }}
        entry_text = "The first thing that God did when he created the universe was to create spheres. Without spheres, no planets. Without planets, no Earth. Without Earth, no humans. Without humans, no DGI course.

        The first step for us and this project is the same. We want to create a solar system with procedurally generated planets. To create these planets, we need spheres! We base our planets on Sebastian Lague's technique for creating spheres. His YouTube series about the topic has inspried this project and will be used to create a basic planet.

        This technique uses a cube to create a sphere since the size of triangles are the same, resulting in an even distribution of detail. Furthermore, the number of triangles are increased at a reasonable rate when the level of detail is increased. One issue with this technique is that, since the sphere is created from the sides of a cube, surface normals do not match up. This can be seen in the image above. It will however be fixed later in this project.
        
        "
        />
        <!-- <JournalEntry
            entry_title = "Sample Entry With Image"
            entry_date = "2023-05-07"
            entry_image =  {{
                src: "exampleimage.jpg",
                id: "1",
                text: "This is space.",
                desc: "space"
             }}
            entry_text = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Mattis vulputate enim nulla aliquet porttitor lacus luctus. In nisl nisi scelerisque eu ultrices vitae auctor eu augue. Id aliquet risus feugiat in ante metus dictum at. Quisque id diam vel quam elementum pulvinar etiam non. Sed blandit libero volutpat sed cras ornare arcu. Aliquam eleifend mi in nulla posuere sollicitudin aliquam ultrices. Diam in arcu cursus euismod quis viverra nibh cras pulvinar. Cursus in hac habitasse platea dictumst. Vulputate dignissim suspendisse in est.

            Egestas dui id ornare arcu odio ut sem. In cursus turpis massa tincidunt dui ut ornare lectus. Semper risus in hendrerit gravida. Erat pellentesque adipiscing commodo elit. Duis ut diam quam nulla porttitor. Ac feugiat sed lectus vestibulum mattis. Lacus vel facilisis volutpat est velit egestas dui id ornare. Gravida cum sociis natoque penatibus. Sit amet consectetur adipiscing elit duis tristique sollicitudin nibh. Neque vitae tempus quam pellentesque nec nam aliquam. At ultrices mi tempus imperdiet nulla. Integer enim neque volutpat ac tincidunt vitae semper. Pellentesque sit amet porttitor eget. Sed turpis tincidunt id aliquet risus feugiat in. Eu consequat ac felis donec. Pulvinar mattis nunc sed blandit libero volutpat sed cras.
            
            Pellentesque sit amet porttitor eget dolor morbi. Eu turpis egestas pretium aenean pharetra magna ac. Amet tellus cras adipiscing enim eu turpis egestas. Morbi tincidunt ornare massa eget. Vel quam elementum pulvinar etiam non quam lacus suspendisse faucibus. Ultrices neque ornare aenean euismod elementum nisi quis eleifend quam. Sapien et ligula ullamcorper malesuada proin libero nunc consequat interdum. Pulvinar sapien et ligula ullamcorper malesuada proin. Leo integer malesuada nunc vel risus commodo viverra maecenas. Donec et odio pellentesque diam volutpat commodo sed egestas egestas. Rhoncus mattis rhoncus urna neque viverra justo nec. Imperdiet nulla malesuada pellentesque elit. Id cursus metus aliquam eleifend. Ac tortor dignissim convallis aenean et.
            
            Nullam vehicula ipsum a arcu cursus vitae congue mauris. Posuere lorem ipsum dolor sit amet consectetur. Turpis egestas maecenas pharetra convallis posuere morbi leo. In cursus turpis massa tincidunt. Fermentum odio eu feugiat pretium nibh. Ornare suspendisse sed nisi lacus sed viverra tellus in hac. In ornare quam viverra orci sagittis eu volutpat odio facilisis. Libero id faucibus nisl tincidunt eget nullam non nisi est. Tincidunt tortor aliquam nulla facilisi cras fermentum. Nisi scelerisque eu ultrices vitae auctor. Enim nunc faucibus a pellentesque. Scelerisque felis imperdiet proin fermentum leo vel orci porta. Amet venenatis urna cursus eget nunc scelerisque. Mattis pellentesque id nibh tortor. Suscipit adipiscing bibendum est ultricies integer quis auctor. Adipiscing diam donec adipiscing tristique risus nec feugiat. Lorem mollis aliquam ut porttitor leo a diam sollicitudin.
            
            Amet massa vitae tortor condimentum lacinia quis vel. Sed euismod nisi porta lorem mollis aliquam ut. Semper risus in hendrerit gravida rutrum quisque non tellus. Fames ac turpis egestas maecenas pharetra convallis posuere morbi leo. Id velit ut tortor pretium. Ullamcorper morbi tincidunt ornare massa. Et netus et malesuada fames ac turpis. Etiam non quam lacus suspendisse faucibus interdum. Metus dictum at tempor commodo ullamcorper a lacus vestibulum. Risus pretium quam vulputate dignissim suspendisse in est ante in. Cursus metus aliquam eleifend mi in nulla posuere sollicitudin aliquam. Urna nunc id cursus metus aliquam eleifend."
        /> -->
    </div>
    <footer>
        <p>KTH DH2323 - <a href="https://github.com/procedural-planets/planets-src" target="_blank" rel="noopener noreferrer">GitHub Repository</a></p>
    </footer>
</main>

<style lang="scss">
	@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,400;0,700;1,400&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,400;0,700;1,400&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400;0,700;1,400&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Righteous&display=swap');

    :global(:root) {
        font-family: 'Lato';
        font-size: 1.5vh;
        background-color: rgb(15, 65, 62);
        color: white;
    }

    :global(h1) {
        font-family: 'EB Garamond';
        font-size: 4.4vh;
        text-align: center;
    }

    :global(h2) {
        font-family: 'EB Garamond';
        font-size: 3vh;
    }

    main {
        width: 50vw;
        height: 100vh;
        margin: auto;
    }

    .title {
        padding-top: 2em;
        padding-bottom: 2em;
    }

    .title p {
        text-align: center;
    }

    footer p {
        text-align: center;
        color:rgb(124, 158, 155)
    }

    footer a {
        color: white;
    }

    footer {
        height: 4em;
    }

    @media only screen and (max-width: 768px) {
        main {
            width: 90vw;
        }
    }
</style>