<svelte:head>
    <title>University of Nizwa - Where Tradition Meets Innovation</title>
    <meta name="description" content="The University of Nizwa combines academic excellence with modern facilities to prepare students for global success. Explore our world-class programs and vibrant campus community." />
</svelte:head>

<script lang="ts">
	import { onMount } from 'svelte';

    // Data for sections
    const navLinks = ["Academics", "Admissions", "Campus Life", "Research", "About"];
    
    const accreditations = [
        { name: "Ministry of Higher Education", width: 120 },
        { name: "AACSB", width: 80 },
        { name: "ABET", width: 70 },
        { name: "QAA", width: 60 },
        { name: "UNESCO", width: 100 },
        { name: "Arab League", width: 90 }
    ];

    const features = [
        {
            tag: "ACADEMIC EXCELLENCE",
            title: "World-class programs accredited internationally",
            image: "/generated/image-students-collaborating-in-a-modern-libra-1766208080538-1.webp",
            color: "bg-gray-100"
        },
        {
            tag: "RESEARCH FACILITIES",
            title: "State-of-the-art laboratories and research centers",
            image: "/generated/image-science-laboratory-with-students-conduct-1766208083055-2.webp",
            color: "bg-gray-100"
        },
        {
            tag: "WORLD-CLASS FACULTY",
            title: "Learn from distinguished scholars and industry experts",
            image: "/generated/image-university-lecture-hall-with-professor-t-1766208085525-3.webp",
            color: "bg-gray-100"
        },
        {
            tag: "VIBRANT CAMPUS LIFE",
            title: "Rich student experience with diverse activities",
            image: "/generated/image-students-participating-in-campus-activit-1766208087979-4.webp",
            color: "bg-gray-100"
        },
        {
            tag: "MODERN FACILITIES",
            title: "Contemporary campus blending tradition and innovation",
            image: "/generated/image-modern-university-building-exterior-with-1766208090711-5.webp",
            color: "bg-gray-100"
        },
        {
            tag: "GLOBAL COMMUNITY",
            title: "International environment preparing you for the world",
            image: "/generated/image-happy-international-students-studying-to-1766208095634-7.webp",
            color: "bg-gray-100"
        }
    ];

    const testimonials = [
        {
            quote: "The University of Nizwa provided me with an exceptional education that prepared me for a successful career in engineering. The faculty's dedication and modern facilities made all the difference.",
            name: "Ahmed Al-Balushi",
            role: "Civil Engineering Graduate, Class of 2023",
            avatar: "AA"
        },
        {
            quote: "Studying at Unizwa was transformative. The blend of traditional values and modern teaching methods created the perfect learning environment.",
            name: "Fatima Al-Rashidi",
            role: "Business Administration Graduate",
            avatar: "FR"
        },
         {
            quote: "The research opportunities at University of Nizwa are outstanding. I was able to work on cutting-edge projects that have shaped my academic career.",
            name: "Dr. Mohammed Al-Hinai",
            role: "PhD Graduate, Now Assistant Professor",
            avatar: "MH"
        },
        {
            quote: "The international community at Unizwa enriched my university experience. I made lifelong friends from around the world while receiving a world-class education.",
            name: "Sarah Johnson",
            role: "International Student, Computer Science",
            avatar: "SJ"
        },
        {
            quote: "The support from faculty and staff at University of Nizwa goes beyond academics. They truly care about student success and personal growth.",
            name: "Khalid Al-Mamari",
            role: "Pharmacy Graduate, Class of 2024",
            avatar: "KM"
        },
        {
            quote: "University of Nizwa's commitment to academic excellence and innovation sets it apart. The skills I gained here have been invaluable in my professional journey.",
            name: "Layla Al-Habsi",
            role: "Law Graduate, Now Practicing Attorney",
            avatar: "LH"
        }
    ];

    const studentSupport = [
        "Academic advising and counseling",
        "Career development services",
        "International student support",
        "Scholarship and financial aid",
        "Student housing assistance",
        "Health and wellness programs",
        "Library and research resources"
    ];

    const programs = [
        {
            tag: "UNDERGRADUATE",
            title: "Bachelor's Degrees",
            description: "Comprehensive programs in Engineering, Business, Sciences, Arts, and more"
        },
        {
            tag: "GRADUATE",
            title: "Master's Programs",
            description: "Advanced studies designed for professional and academic advancement"
        },
        {
            tag: "DOCTORAL",
            title: "PhD Programs",
            description: "Research-intensive programs leading to doctoral degrees in various fields"
        },
        {
            tag: "PROFESSIONAL",
            title: "Professional Development",
            description: "Continuing education and certificate programs for working professionals"
        },
        {
            tag: "RESEARCH",
            title: "Research Centers",
            description: "State-of-the-art facilities supporting groundbreaking research initiatives"
        }
    ];

    const faqs = [
        "What programs does the University of Nizwa offer?",
        "How do I apply for admission?",
        "What are the tuition fees and scholarship opportunities?",
        "Does the university accept international students?",
        "What is campus life like at University of Nizwa?",
        "Are there accommodation options for students?",
        "What career support services are available?",
        "Is the university accredited?",
        "How can I schedule a campus visit?"
    ];

</script>

<div class="font-sans text-gray-900 bg-white selection:bg-primary-200 selection:text-black">
    <!-- Navbar -->
    <nav class="sticky top-0 z-50 bg-white/80 backdrop-blur-md border-b border-gray-100">
        <div class="max-w-[1400px] mx-auto px-6 h-16 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <!-- Logo Mark -->
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="text-primary-600">
                    <path
                        fill-rule="evenodd"
                        clip-rule="evenodd"
                        d="M6.99251 12.196C6.85314 12.5757 6.62925 12.9208 6.33682 13.2067H6.33835C6.00191 13.5351 5.58566 13.7756 5.12816 13.9059C4.67065 14.0362 4.18671 14.0522 3.72118 13.9523C3.25564 13.8524 2.82357 13.64 2.46501 13.3345C2.10645 13.0291 1.83299 12.6406 1.66998 12.2051C1.50697 11.7696 1.45969 11.3012 1.5325 10.8432C1.60532 10.3852 1.79587 9.95244 2.08653 9.58516C2.37718 9.21781 2.75852 8.9277 3.1952 8.74177C3.63188 8.55585 4.10979 8.48002 4.58462 8.52142L4.57074 8.50792C5.0567 8.54782 5.54575 8.48407 6.00378 8.32124C6.4618 8.15846 6.87776 7.90043 7.2226 7.56521C7.56746 7.22998 7.83285 6.82564 8.00036 6.38041C8.16786 5.93517 8.23344 5.45976 8.1924 4.98737L8.20628 5.00087C8.15181 4.43594 8.27796 3.86844 8.56753 3.37575C8.85701 2.88307 9.29579 2.48919 9.82407 2.24782C10.3523 2.00645 10.9443 1.92933 11.5192 2.02701C12.0942 2.12467 12.6243 2.39237 13.037 2.79358C13.4497 3.19479 13.7251 3.70999 13.8256 4.26892C13.926 4.82785 13.8467 5.4033 13.5984 5.9168C13.3501 6.4303 12.9449 6.85685 12.4381 7.13828C11.9313 7.41971 11.3474 7.54233 10.7663 7.4894L10.781 7.5029C10.2949 7.46279 9.80563 7.52632 9.34741 7.68904C8.88919 7.85176 8.47309 8.10975 8.12805 8.44499C7.78301 8.78025 7.51742 9.18466 7.34983 9.63001C7.18224 10.0754 7.11669 10.551 7.15774 11.0235L7.14309 11.01C7.1833 11.4112 7.13189 11.8162 6.99251 12.196ZM11.5077 14.7121L11.493 14.6986C11.9061 14.739 12.3232 14.6897 12.7143 14.5543C13.1053 14.4188 13.4605 14.2007 13.7542 13.9154C14.0477 13.6302 14.2726 13.285 14.4121 12.905C14.5518 12.525 14.6028 12.1196 14.5615 11.718L14.5762 11.7315C14.5351 11.2591 14.6007 10.7838 14.7681 10.3385C14.9356 9.89327 15.2011 9.48893 15.5459 9.15368C15.8908 8.8185 16.3068 8.56042 16.7648 8.39767C17.2228 8.23481 17.7118 8.17111 18.1978 8.21099L18.1832 8.19749C18.7645 8.25059 19.3485 8.12801 19.8556 7.84656C20.3627 7.56511 20.7681 7.13845 21.0165 6.62479C21.265 6.11114 21.3444 5.53548 21.2439 4.97634C21.1435 4.4172 20.868 3.9018 20.4551 3.50044C20.0422 3.09909 19.512 2.8313 18.9368 2.73364C18.3616 2.63596 17.7695 2.71315 17.241 2.95467C16.7126 3.19618 16.2737 3.59027 15.9842 4.08319C15.6946 4.57609 15.5685 5.14383 15.6232 5.70895L15.6093 5.6947C15.6504 6.16712 15.585 6.64259 15.4175 7.08788C15.2501 7.53318 14.9846 7.93758 14.6398 8.27287C14.2949 8.60805 13.8789 8.86612 13.4208 9.02888C12.9627 9.19163 12.4736 9.25523 11.9876 9.21526L12.0015 9.22951C11.5885 9.18908 11.1713 9.23836 10.7803 9.37381C10.3893 9.50919 10.034 9.72744 9.74039 10.0127C9.44674 10.2979 9.22199 10.6431 9.08234 11.0231C8.94276 11.4031 8.89176 11.8085 8.93304 12.2101L8.91915 12.1966C8.96005 12.6689 8.89439 13.1443 8.72688 13.5895C8.5593 14.0346 8.29389 14.4389 7.94908 14.7741C7.60425 15.1093 7.18835 15.3673 6.73039 15.5302C6.27242 15.693 5.78342 15.7569 5.29749 15.7171L5.31138 15.7306C4.73003 15.6775 4.14599 15.8001 3.63892 16.0815C3.13186 16.363 2.72644 16.7896 2.478 17.3033C2.22954 17.817 2.15013 18.3926 2.25061 18.9518C2.35109 19.5109 2.62657 20.0263 3.03945 20.4276C3.45234 20.829 3.98253 21.0968 4.55773 21.1944C5.13293 21.2921 5.72512 21.2149 6.25353 20.9734C6.78193 20.7319 7.22085 20.3379 7.51038 19.8449C7.79994 19.352 7.92601 18.7843 7.87139 18.2191L7.88605 18.2326C7.845 17.7602 7.91058 17.2849 8.07809 16.8396C8.24551 16.3944 8.511 15.99 8.85581 15.6548C9.20069 15.3196 9.61664 15.0615 10.0746 14.8988C10.5327 14.7359 11.0217 14.6722 11.5077 14.7121ZM17.1996 10.7633C16.9071 11.0493 16.6832 11.3944 16.5437 11.7741C16.4042 12.1538 16.3526 12.5587 16.3925 12.9601L16.3786 12.9466C16.4197 13.419 16.3541 13.8944 16.1866 14.3396C16.0191 14.7849 15.7537 15.1892 15.4089 15.5244C15.064 15.8596 14.648 16.1177 14.19 16.2804C13.732 16.4433 13.2429 16.507 12.757 16.4671L12.7708 16.4806C12.1896 16.4281 11.6057 16.551 11.0989 16.8328C10.5921 17.1145 10.1871 17.5414 9.93902 18.0551C9.69097 18.5689 9.61188 19.1444 9.71265 19.7035C9.81349 20.2625 10.0892 20.7777 10.5022 21.1788C10.9152 21.5799 11.4454 21.8474 12.0205 21.9448C12.5957 22.0423 13.1877 21.9649 13.716 21.7234C14.2443 21.4817 14.683 21.0877 14.9724 20.5947C15.2618 20.1018 15.3878 19.5342 15.3332 18.9692L15.3478 18.9827C15.3068 18.5103 15.3723 18.0349 15.5398 17.5896C15.7073 17.1444 15.9728 16.7401 16.3176 16.4048C16.6625 16.0696 17.0784 15.8115 17.5364 15.6488C17.9945 15.486 18.4835 15.4222 18.9695 15.4621L18.9548 15.4486C19.4296 15.4901 19.9076 15.4144 20.3444 15.2286C20.7811 15.0427 21.1625 14.7527 21.4533 14.3854C21.744 14.0181 21.9347 13.5854 22.0075 13.1274C22.0805 12.6694 22.0332 12.2009 21.8703 11.7653C21.7073 11.3298 21.4339 10.9413 21.0754 10.6358C20.7168 10.3303 20.2848 10.1178 19.8192 10.0179C19.3536 9.91795 18.8697 9.93385 18.4121 10.0641C17.9546 10.1945 17.5383 10.4349 17.2019 10.7633H17.1996Z"
                        fill="currentColor"
                    />
                </svg>
                <span class="font-medium text-lg tracking-tight">University of Nizwa</span>
            </div>

            <div class="hidden md:flex items-center gap-8 text-sm font-medium text-gray-600">
                {#each navLinks as link}
                    <a href="#" class="hover:text-primary-600 transition-colors">{link}</a>
                {/each}
            </div>

            <button class="bg-primary-600 text-white px-5 py-2 rounded-full text-sm font-medium hover:bg-primary-700 transition-colors">
                Apply Now
            </button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="pt-20 pb-16 px-6 text-center overflow-hidden">
        <div class="max-w-4xl mx-auto mb-12">
            <h1 class="font-serif text-6xl md:text-7xl lg:text-[5rem] leading-[1.1] mb-6 font-normal tracking-tight">
                Where tradition meets <br/> innovation in education
            </h1>
            <p class="text-lg md:text-xl text-gray-600 max-w-2xl mx-auto mb-8 leading-relaxed">
                The University of Nizwa combines academic excellence with modern facilities to prepare students for global success.
            </p>
            <button class="bg-primary-600 text-white px-8 py-3 rounded-full text-base font-medium hover:bg-primary-700 transition-colors">
                Explore Programs
            </button>
        </div>

        <!-- Hero Image -->
        <div class="relative max-w-[1400px] mx-auto h-[400px] md:h-[600px] mt-12 rounded-3xl overflow-hidden shadow-2xl">
            <img 
                src="/generated/image-modern-university-campus-with-students-w-1766208076982-0.webp" 
                alt="University of Nizwa Campus" 
                class="w-full h-full object-cover"
            />
            <div class="absolute inset-0 bg-gradient-to-t from-black/40 to-transparent"></div>
        </div>
    </section>

    <!-- Accreditations Section -->
    <section class="py-16 border-b border-gray-100">
        <div class="max-w-[1400px] mx-auto px-6 text-center">
            <p class="text-sm text-gray-500 mb-10">Internationally accredited and recognized</p>
            <div class="flex flex-wrap justify-center items-center gap-12 md:gap-16 opacity-70 grayscale hover:grayscale-0 transition-all duration-500">
                {#each accreditations as accreditation}
                    <div class="h-8 flex items-center justify-center">
                        <span class="font-bold text-lg text-gray-700">{accreditation.name}</span>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Why Choose Unizwa Grid -->
    <section class="py-24 px-6 bg-gray-50">
        <div class="max-w-[1400px] mx-auto">
            <div class="text-center max-w-3xl mx-auto mb-20">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">Why Choose Unizwa</h2>
                <p class="text-lg text-gray-600 leading-relaxed">
                    The University of Nizwa offers a comprehensive educational experience that combines academic rigor with practical skills, preparing students for successful careers in a global marketplace.
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                {#each features as feature}
                    <div class="group bg-white rounded-2xl overflow-hidden shadow-sm hover:shadow-md transition-shadow duration-300 flex flex-col">
                        <div class="p-8">
                            <span class="inline-block bg-primary-100 text-primary-700 text-[10px] font-bold tracking-wider px-2 py-1 rounded mb-4 uppercase">
                                {feature.tag}
                            </span>
                            <h3 class="font-serif text-2xl leading-tight mb-4">
                                {feature.title}
                            </h3>
                        </div>
                        <div class="h-[300px] relative overflow-hidden">
                            <img 
                                src={feature.image} 
                                alt={feature.title}
                                class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500"
                            />
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="py-24 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
            <div class="text-center max-w-3xl mx-auto mb-20">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">Student Success Stories</h2>
                <p class="text-lg text-gray-600 leading-relaxed mb-10">
                    Hear from our graduates and current students about their transformative experiences at the University of Nizwa.
                </p>
            </div>

            <div class="columns-1 md:columns-2 lg:columns-3 gap-6 space-y-6">
                {#each testimonials as testimonial}
                    <div class="break-inside-avoid bg-gray-50 p-8 rounded-2xl border border-gray-100">
                        <p class="text-lg leading-relaxed mb-6">"{testimonial.quote}"</p>
                        <div class="flex items-center gap-3">
                            <div class="w-10 h-10 bg-primary-200 rounded-full flex items-center justify-center text-sm font-bold text-primary-700">
                                {testimonial.avatar}
                            </div>
                            <div>
                                <div class="font-medium">{testimonial.name}</div>
                                <div class="text-sm text-gray-500">{testimonial.role}</div>
                            </div>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Student Support Section -->
    <section class="py-24 px-6 bg-white border-t border-gray-100">
        <div class="max-w-[1400px] mx-auto">
             <div class="text-center max-w-3xl mx-auto mb-20">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">Comprehensive <br/> Student Support</h2>
                <p class="text-lg text-gray-600 leading-relaxed">
                    At the University of Nizwa, we're committed to your success both inside and outside the classroom.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div class="bg-gray-50 p-12 rounded-3xl h-full border border-gray-100">
                    <h3 class="font-serif text-2xl mb-8">Support Services</h3>
                    <ul class="space-y-4">
                        {#each studentSupport as service}
                            <li class="flex items-center gap-3">
                                <div class="w-5 h-5 rounded-full bg-primary-500 flex items-center justify-center shrink-0">
                                    <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"></polyline></svg>
                                </div>
                                <span class="text-gray-700">{service}</span>
                            </li>
                        {/each}
                    </ul>
                </div>
                <div class="h-full min-h-[500px] rounded-3xl overflow-hidden relative shadow-lg">
                    <img 
                        src="/generated/image-confident-young-graduate-in-cap-and-gown-1766208093250-6.webp" 
                        alt="Successful Graduate"
                        class="w-full h-full object-cover"
                    />
                </div>
            </div>
        </div>
    </section>

    <!-- Academic Programs Section -->
    <section class="py-24 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">Academic Programs</h2>
                <p class="text-lg text-gray-600">Explore our diverse range of programs designed to prepare you for success.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                {#each programs as program}
                    <div class="bg-gray-50 p-8 rounded-2xl border border-gray-100 hover:shadow-lg transition-shadow duration-300">
                        <span class="inline-block bg-primary-100 text-primary-700 text-[10px] font-bold tracking-wider px-2 py-1 rounded mb-4 uppercase">
                            {program.tag}
                        </span>
                        <h3 class="font-serif text-2xl mb-4">{program.title}</h3>
                        <p class="text-gray-600 leading-relaxed">{program.description}</p>
                        <button class="mt-6 text-primary-600 font-medium hover:text-primary-700 transition-colors">
                            Learn more →
                        </button>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Campus Life Section -->
    <section class="py-24 px-6 bg-gray-50">
        <div class="max-w-[1400px] mx-auto">
             <div class="text-center max-w-3xl mx-auto mb-20">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">Experience Campus Life</h2>
                <p class="text-lg text-gray-600 leading-relaxed">
                    Beyond academics, the University of Nizwa offers a vibrant campus community with diverse opportunities for personal growth and cultural enrichment.
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="bg-white p-12 rounded-3xl border border-gray-100">
                    <h3 class="font-serif text-3xl mb-6">Student Organizations</h3>
                    <p class="text-gray-600 leading-relaxed mb-6">
                        Join over 50 student clubs and organizations covering academic interests, cultural activities, sports, and community service.
                    </p>
                    <ul class="space-y-3 text-gray-700">
                        <li class="flex items-center gap-2">
                            <span class="text-primary-600">•</span> Academic and Professional Societies
                        </li>
                        <li class="flex items-center gap-2">
                            <span class="text-primary-600">•</span> Cultural and Arts Groups
                        </li>
                        <li class="flex items-center gap-2">
                            <span class="text-primary-600">•</span> Sports and Recreation Teams
                        </li>
                        <li class="flex items-center gap-2">
                            <span class="text-primary-600">•</span> Community Service Initiatives
                        </li>
                    </ul>
                </div>
                <div class="bg-white p-12 rounded-3xl border border-gray-100">
                    <h3 class="font-serif text-3xl mb-6">Campus Facilities</h3>
                    <p class="text-gray-600 leading-relaxed mb-6">
                        State-of-the-art facilities designed to support your academic journey and personal development.
                    </p>
                    <ul class="space-y-3 text-gray-700">
                        <li class="flex items-center gap-2">
                            <span class="text-primary-600">•</span> Modern Library and Learning Commons
                        </li>
                        <li class="flex items-center gap-2">
                            <span class="text-primary-600">•</span> Sports Complex and Fitness Center
                        </li>
                        <li class="flex items-center gap-2">
                            <span class="text-primary-600">•</span> Student Center and Dining Halls
                        </li>
                        <li class="flex items-center gap-2">
                            <span class="text-primary-600">•</span> Innovation Labs and Maker Spaces
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Global Partnerships Section -->
    <section class="py-24 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
             <div class="text-center max-w-3xl mx-auto mb-20">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">Global Partnerships <br/> & Recognition</h2>
                <p class="text-lg text-gray-600 leading-relaxed">
                    The University of Nizwa maintains strong partnerships with leading institutions worldwide and holds prestigious accreditations.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-16">
                <!-- International Partnerships -->
                <div>
                    <div class="text-center mb-8">
                        <span class="bg-primary-100 text-primary-700 text-[10px] font-bold tracking-wider px-2 py-1 rounded uppercase">
                            INTERNATIONAL COLLABORATIONS
                        </span>
                    </div>
                    <div class="grid grid-cols-3 gap-6">
                        {#each ['University Exchange Programs', 'Research Partnerships', 'Faculty Exchange', 'Joint Degrees', 'Study Abroad', 'International Conferences', 'Global Research Networks', 'Industry Partnerships', 'Innovation Hubs'] as partnership}
                            <div class="aspect-square bg-gray-50 rounded-xl flex flex-col items-center justify-center p-4 hover:bg-gray-100 transition-colors border border-gray-100">
                                <span class="text-[11px] text-center text-gray-700 font-medium leading-tight">{partnership}</span>
                            </div>
                        {/each}
                    </div>
                </div>

                <!-- Accreditations -->
                <div>
                    <div class="text-center mb-8">
                        <span class="bg-primary-100 text-primary-700 text-[10px] font-bold tracking-wider px-2 py-1 rounded uppercase">
                            ACCREDITATIONS & CERTIFICATIONS
                        </span>
                    </div>
                    <div class="grid grid-cols-3 gap-6">
                         {#each ['Ministry Approved', 'AACSB Accredited', 'ABET Certified', 'ISO 9001', 'QAA Recognition', 'Research Excellence', 'Academic Quality', 'International Standards', 'Professional Bodies'] as accreditation}
                            <div class="aspect-square bg-gray-50 rounded-xl flex flex-col items-center justify-center p-4 hover:bg-gray-100 transition-colors border border-gray-100">
                                <span class="text-[11px] text-center text-gray-700 font-medium leading-tight">{accreditation}</span>
                            </div>
                        {/each}
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Mission Section -->
    <section class="py-24 px-6">
        <div class="max-w-[1400px] mx-auto grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
            <div class="rounded-3xl overflow-hidden shadow-xl">
                <img 
                    src="/generated/image-modern-university-building-exterior-with-1766208090711-5.webp" 
                    alt="University of Nizwa Campus"
                    class="w-full h-[600px] object-cover"
                />
            </div>
            <div class="bg-primary-50 p-12 lg:p-16 rounded-3xl border border-primary-100">
                <h2 class="font-serif text-4xl md:text-5xl mb-8 text-primary-900">Our Mission</h2>
                <p class="font-serif text-xl md:text-2xl leading-relaxed mb-6 text-gray-800">
                    The University of Nizwa is dedicated to providing world-class education that combines Islamic values with modern academic excellence.
                </p>
                <p class="text-lg leading-relaxed text-gray-700">
                    We strive to develop well-rounded graduates who are equipped with the knowledge, skills, and ethical foundation to contribute meaningfully to society and excel in an increasingly interconnected world.
                </p>
            </div>
        </div>
    </section>

    <!-- Bottom CTA -->
    <section class="py-32 px-6 text-center bg-white">
        <div class="max-w-4xl mx-auto">
            <h2 class="font-serif text-6xl md:text-7xl mb-6">Begin your journey <br/> to excellence</h2>
            <p class="text-xl text-gray-600 mb-10">Join the University of Nizwa community today</p>
            <div class="flex gap-4 justify-center">
                <button class="bg-primary-600 text-white px-8 py-3 rounded-full text-base font-medium hover:bg-primary-700 transition-colors">
                    Apply Now
                </button>
                <button class="bg-white text-primary-600 border-2 border-primary-600 px-8 py-3 rounded-full text-base font-medium hover:bg-primary-50 transition-colors">
                    Schedule a Visit
                </button>
            </div>
        </div>
    </section>

    <!-- FAQ Section -->
    <section class="py-24 px-6 bg-white border-t border-gray-100">
        <div class="max-w-[1400px] mx-auto">
            <h2 class="font-serif text-5xl mb-16">FAQ</h2>
            <div class="space-y-4">
                {#each faqs as faq}
                    <div class="border-b border-gray-100 py-6 flex justify-between items-center cursor-pointer group hover:bg-gray-50 px-4 -mx-4 rounded-lg transition-colors">
                        <span class="text-lg font-medium">{faq}</span>
                        <div class="w-8 h-8 rounded-full bg-black text-white flex items-center justify-center group-hover:bg-gray-800 transition-colors">
                            <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><line x1="12" y1="5" x2="12" y2="19"></line><line x1="5" y1="12" x2="19" y2="12"></line></svg>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-24 px-6 bg-white border-t border-gray-100">
        <div class="max-w-[1400px] mx-auto grid grid-cols-1 md:grid-cols-4 gap-12">
            <div class="col-span-1 md:col-span-1">
                <div class="flex items-center gap-2 mb-8">
                     <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="text-primary-600">
                        <path
                            fill-rule="evenodd"
                            clip-rule="evenodd"
                            d="M6.99251 12.196C6.85314 12.5757 6.62925 12.9208 6.33682 13.2067H6.33835C6.00191 13.5351 5.58566 13.7756 5.12816 13.9059C4.67065 14.0362 4.18671 14.0522 3.72118 13.9523C3.25564 13.8524 2.82357 13.64 2.46501 13.3345C2.10645 13.0291 1.83299 12.6406 1.66998 12.2051C1.50697 11.7696 1.45969 11.3012 1.5325 10.8432C1.60532 10.3852 1.79587 9.95244 2.08653 9.58516C2.37718 9.21781 2.75852 8.9277 3.1952 8.74177C3.63188 8.55585 4.10979 8.48002 4.58462 8.52142L4.57074 8.50792C5.0567 8.54782 5.54575 8.48407 6.00378 8.32124C6.4618 8.15846 6.87776 7.90043 7.2226 7.56521C7.56746 7.22998 7.83285 6.82564 8.00036 6.38041C8.16786 5.93517 8.23344 5.45976 8.1924 4.98737L8.20628 5.00087C8.15181 4.43594 8.27796 3.86844 8.56753 3.37575C8.85701 2.88307 9.29579 2.48919 9.82407 2.24782C10.3523 2.00645 10.9443 1.92933 11.5192 2.02701C12.0942 2.12467 12.6243 2.39237 13.037 2.79358C13.4497 3.19479 13.7251 3.70999 13.8256 4.26892C13.926 4.82785 13.8467 5.4033 13.5984 5.9168C13.3501 6.4303 12.9449 6.85685 12.4381 7.13828C11.9313 7.41971 11.3474 7.54233 10.7663 7.4894L10.781 7.5029C10.2949 7.46279 9.80563 7.52632 9.34741 7.68904C8.88919 7.85176 8.47309 8.10975 8.12805 8.44499C7.78301 8.78025 7.51742 9.18466 7.34983 9.63001C7.18224 10.0754 7.11669 10.551 7.15774 11.0235L7.14309 11.01C7.1833 11.4112 7.13189 11.8162 6.99251 12.196ZM11.5077 14.7121L11.493 14.6986C11.9061 14.739 12.3232 14.6897 12.7143 14.5543C13.1053 14.4188 13.4605 14.2007 13.7542 13.9154C14.0477 13.6302 14.2726 13.285 14.4121 12.905C14.5518 12.525 14.6028 12.1196 14.5615 11.718L14.5762 11.7315C14.5351 11.2591 14.6007 10.7838 14.7681 10.3385C14.9356 9.89327 15.2011 9.48893 15.5459 9.15368C15.8908 8.8185 16.3068 8.56042 16.7648 8.39767C17.2228 8.23481 17.7118 8.17111 18.1978 8.21099L18.1832 8.19749C18.7645 8.25059 19.3485 8.12801 19.8556 7.84656C20.3627 7.56511 20.7681 7.13845 21.0165 6.62479C21.265 6.11114 21.3444 5.53548 21.2439 4.97634C21.1435 4.4172 20.868 3.9018 20.4551 3.50044C20.0422 3.09909 19.512 2.8313 18.9368 2.73364C18.3616 2.63596 17.7695 2.71315 17.241 2.95467C16.7126 3.19618 16.2737 3.59027 15.9842 4.08319C15.6946 4.57609 15.5685 5.14383 15.6232 5.70895L15.6093 5.6947C15.6504 6.16712 15.585 6.64259 15.4175 7.08788C15.2501 7.53318 14.9846 7.93758 14.6398 8.27287C14.2949 8.60805 13.8789 8.86612 13.4208 9.02888C12.9627 9.19163 12.4736 9.25523 11.9876 9.21526L12.0015 9.22951C11.5885 9.18908 11.1713 9.23836 10.7803 9.37381C10.3893 9.50919 10.034 9.72744 9.74039 10.0127C9.44674 10.2979 9.22199 10.6431 9.08234 11.0231C8.94276 11.4031 8.89176 11.8085 8.93304 12.2101L8.91915 12.1966C8.96005 12.6689 8.89439 13.1443 8.72688 13.5895C8.5593 14.0346 8.29389 14.4389 7.94908 14.7741C7.60425 15.1093 7.18835 15.3673 6.73039 15.5302C6.27242 15.693 5.78342 15.7569 5.29749 15.7171L5.31138 15.7306C4.73003 15.6775 4.14599 15.8001 3.63892 16.0815C3.13186 16.363 2.72644 16.7896 2.478 17.3033C2.22954 17.817 2.15013 18.3926 2.25061 18.9518C2.35109 19.5109 2.62657 20.0263 3.03945 20.4276C3.45234 20.829 3.98253 21.0968 4.55773 21.1944C5.13293 21.2921 5.72512 21.2149 6.25353 20.9734C6.78193 20.7319 7.22085 20.3379 7.51038 19.8449C7.79994 19.352 7.92601 18.7843 7.87139 18.2191L7.88605 18.2326C7.845 17.7602 7.91058 17.2849 8.07809 16.8396C8.24551 16.3944 8.511 15.99 8.85581 15.6548C9.20069 15.3196 9.61664 15.0615 10.0746 14.8988C10.5327 14.7359 11.0217 14.6722 11.5077 14.7121ZM17.1996 10.7633C16.9071 11.0493 16.6832 11.3944 16.5437 11.7741C16.4042 12.1538 16.3526 12.5587 16.3925 12.9601L16.3786 12.9466C16.4197 13.419 16.3541 13.8944 16.1866 14.3396C16.0191 14.7849 15.7537 15.1892 15.4089 15.5244C15.064 15.8596 14.648 16.1177 14.19 16.2804C13.732 16.4433 13.2429 16.507 12.757 16.4671L12.7708 16.4806C12.1896 16.4281 11.6057 16.551 11.0989 16.8328C10.5921 17.1145 10.1871 17.5414 9.93902 18.0551C9.69097 18.5689 9.61188 19.1444 9.71265 19.7035C9.81349 20.2625 10.0892 20.7777 10.5022 21.1788C10.9152 21.5799 11.4454 21.8474 12.0205 21.9448C12.5957 22.0423 13.1877 21.9649 13.716 21.7234C14.2443 21.4817 14.683 21.0877 14.9724 20.5947C15.2618 20.1018 15.3878 19.5342 15.3332 18.9692L15.3478 18.9827C15.3068 18.5103 15.3723 18.0349 15.5398 17.5896C15.7073 17.1444 15.9728 16.7401 16.3176 16.4048C16.6625 16.0696 17.0784 15.8115 17.5364 15.6488C17.9945 15.486 18.4835 15.4222 18.9695 15.4621L18.9548 15.4486C19.4296 15.4901 19.9076 15.4144 20.3444 15.2286C20.7811 15.0427 21.1625 14.7527 21.4533 14.3854C21.744 14.0181 21.9347 13.5854 22.0075 13.1274C22.0805 12.6694 22.0332 12.2009 21.8703 11.7653C21.7073 11.3298 21.4339 10.9413 21.0754 10.6358C20.7168 10.3303 20.2848 10.1178 19.8192 10.0179C19.3536 9.91795 18.8697 9.93385 18.4121 10.0641C17.9546 10.1945 17.5383 10.4349 17.2019 10.7633H17.1996Z"
                            fill="currentColor"
                        />
                    </svg>
                    <span class="font-medium text-xl tracking-tight">University of Nizwa</span>
                </div>
                <div class="text-sm text-gray-500 mb-4">Subscribe to our newsletter</div>
                <div class="flex gap-2 border-b border-gray-200 pb-2 mb-8">
                    <input type="email" placeholder="Email address" class="w-full outline-none text-sm" />
                    <button class="text-gray-400 hover:text-black">→</button>
                </div>
                <div class="text-xs text-gray-400">© University of Nizwa 2025</div>
            </div>

            <div class="grid grid-cols-2 md:grid-cols-3 gap-8 col-span-1 md:col-span-3">
                <div>
                    <h4 class="text-xs font-bold text-gray-400 uppercase tracking-wider mb-6">Academics</h4>
                    <ul class="space-y-3 text-sm text-gray-600">
                        <li><a href="#" class="hover:text-primary-600">Programs</a></li>
                        <li><a href="#" class="hover:text-primary-600">Undergraduate</a></li>
                        <li><a href="#" class="hover:text-primary-600">Graduate</a></li>
                        <li><a href="#" class="hover:text-primary-600">Doctoral</a></li>
                        <li><a href="#" class="hover:text-primary-600">Colleges</a></li>
                        <li><a href="#" class="hover:text-primary-600">Faculty</a></li>
                        <li><a href="#" class="hover:text-primary-600">Academic Calendar</a></li>
                        <li><a href="#" class="hover:text-primary-600">Library</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-xs font-bold text-gray-400 uppercase tracking-wider mb-6">Admissions</h4>
                    <ul class="space-y-3 text-sm text-gray-600">
                        <li><a href="#" class="hover:text-primary-600">Apply Now</a></li>
                        <li><a href="#" class="hover:text-primary-600">Requirements</a></li>
                        <li><a href="#" class="hover:text-primary-600">Tuition & Fees</a></li>
                        <li><a href="#" class="hover:text-primary-600">Scholarships</a></li>
                        <li><a href="#" class="hover:text-primary-600">International Students</a></li>
                        <li><a href="#" class="hover:text-primary-600">Visit Campus</a></li>
                        <li><a href="#" class="hover:text-primary-600">Contact Admissions</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-xs font-bold text-gray-400 uppercase tracking-wider mb-6">University</h4>
                    <ul class="space-y-3 text-sm text-gray-600">
                        <li><a href="#" class="hover:text-primary-600">About Us</a></li>
                        <li><a href="#" class="hover:text-primary-600">Mission & Vision</a></li>
                        <li><a href="#" class="hover:text-primary-600">Campus Life</a></li>
                        <li><a href="#" class="hover:text-primary-600">Research</a></li>
                        <li><a href="#" class="hover:text-primary-600">News & Events</a></li>
                        <li><a href="#" class="hover:text-primary-600">Careers</a></li>
                        <li><a href="#" class="hover:text-primary-600">Contact Us</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>

</div>

