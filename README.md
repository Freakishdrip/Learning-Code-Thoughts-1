# Learning-Code-Thoughts-1 3rd first week

The first week of the coding bootcamp had a great start. We went over many coding concepts to help think more programmically. We started with easier to understand languages HTML, JavaScript, and CSS. I had taken a similar coding course at Harvard as well as having a hobby of working with electricity. So many of these concepts and logic gates were not new to me. The syntax of how those languages implement the logic flow so far is my biggest trouble area. As well as the feeling of confusion when theoretically the code should work, but doesn't (because of a missing comma or typo), is universally frustrating. However, I am very happy with how professional and knowledgeable the instructors are. 

The first 3 weeks I had learned how to use event listeners, access and change data in a JSON database, set up my own local website, fetch requests, forEach, using the Event variable, using the DOM, making changes to a websites look and features with JavaScript instead of HTML, getting user input. Most importantly, working with a team of people on a project. Everyone has their own methods depending how much they know what they are comfortable using. My previous history as a salesman has helped ease the collaborating process. 

There is a certain meditative process that happens as well when coding. Just you and the computer "talking", very literally about the logic that needs to happen for the program to work. It feels amazing when all of your thoughts are flowing, and your completely in the zone. 

Alternatively, the process of having to literally describe every single step precisely can get tedious at times. Its like the excerise that some parents or teachers give to children. The parent or teacher tell the child to write down all the steps of making a peanut butter sandwich. If the child were to write down a step as "Now put the butter knife in the peanut butter", the parent or teacher would put the knife in handle first. Often times this leads to frustration of the child but is an important lesson in specificity. Same thing happens in coding as well, a phrase that isn't completely defined will often lead to the program throwing an error. Most of all coding and working in this type of logic environment is an excerise of patience.

One of the first ungoogle-able problems I had with my website was in this snippet of code below.

function searchProducts(data, query) {
        console.log(query)
        console.log(data)
        let searchWord = query.toLowerCase()
        let filteredProducts = data.filter(product =>
            product["product_type"].toLowerCase().includes(searchWord) ||   
            product.brand.toLowerCase().includes(searchWord) || 
            product.name.toLowerCase().includes(searchWord) ||
            product.brand.toLowerCase().includes(searchWord)
        )

        console.log(filteredProducts)

        displayProducts(filteredProducts);
    }

The context of this code is that we are adding a function that will take user input from a search bar, sort what the user is looking for, then pass that information to the display function. The trouble with this begins at line 17. Every single time I tried to run this it was giving the error of .filter is not defined. For more experinced coders this should be a moderately easy solution to find. Unfortunately, Google was no help in this situation, ChatGDP couldn't help find a solution. For this was the ultimate error, the logic works however this function did not work! Here's the solution to the code. 

function searchProducts(data, query) {
        console.log(query)
        console.log(data)
        let searchWord = query.toLowerCase()
        let filteredProducts = data?.filter(product =>
            product["product_type"]?.toLowerCase().includes(searchWord) ||   
            product.brand?.toLowerCase().includes(searchWord) || 
            product.name?.toLowerCase().includes(searchWord) ||
            product.brand?.toLowerCase().includes(searchWord)
        )

        console.log(filteredProducts)

        displayProducts(filteredProducts);
    }

If you are having trouble finding how the code is changed, there is no shame in it. The solution was to put the "?" after the item it was looking for. The reason that the question marks are needed is because while the logic looks good the code is not able to move forward if it cannot find that specific item. 

While my life has had its twists and turns in my career path, I really feel a deeper connection to this. It is stimulating, enagaging, and I can always learn more. My previous jobs of being a door to door salesman and being a trucker was atleast engaging, I never felt like it was the right place for me to be. 

While coding has it challenges it can be rewarding as well. The feeling of finally seeing the finished project get made and work exactly how you wanted it too feels incredible. Like seeing your baby take steps for the first time. Deciding to learn coding is very stressful but exciting time in my life. The journey I have started with this will hopefully change the world for the better. My end goal for coding is to learn how to code robots that will help clean up our streets, our rivers, our oceans, and our lives. 









It is very exciting to have finally taken this leap in life. From salesman of 3 years to trucker to coder life has been a journey so far. I am hoping for the pacing to pick up here
