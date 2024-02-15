# WordPress, PHP, and HTML Websites on Android Platform

<hr>


<p align="center">
    <img src="slides/1_introduction.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>



<p align="center">
    <img src="slides/2_timeline_web_tech.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ Brief Timeline of Relevant Web Technologies

The dawn of the internet age emerged with the inception of ARPANET in 1969, laying the groundwork for the expansive web ecosystem we navigate today. Notably, ARM architecture entered the market in 1983, marking a pivotal moment in the evolution of mobile chipsets and devices. This evolution culminated in the introduction of Android smartphones in 2008, ushering in a new era of mobile computing.

Despite the widespread adoption of Android smartphones, research and development remains scarce concerning web servers on these devices. Recognizing this gap, I embarked on a quest to explore the feasibility of deploying web servers on Android devices. Through a series of rigorous tests and benchmarking analyses, I sought to shed light on the potential of leveraging Android devices as web servers in daily operations.
<hr>

<p align="center">
    <img src="slides/3_1st_web.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ 1st Website and Web Browsers

Before delving into the intricacies of Android servers, let's take a moment to rewind and explore the origins of the web, starting with the first website in 1991. At its inception, the World Wide Web was a humble project initiated by Tim Berners-Lee at CERN, designed to facilitate the sharing of information among researchers.

In 1991, the first website was a rudimentary affair, accessible only through terminal interfaces. Users navigated through text-based pages using simple commands, accessing basic HTML content that straightforwardly conveyed information.

Fast forward to 1993, and the web experienced a significant evolution with the introduction of web browsers. The release of Mosaic, the first graphical web browser, transformed the web browsing experience by enabling users to navigate visually rich content with images, hyperlinks, and formatted text.

Compared to the stark simplicity of terminal-based browsing, the web in 1993 was a revelation, offering a more immersive and user-friendly interface. With the advent of web browsers, the web became accessible to a broader audience, paving the way for its exponential growth and the vibrant digital landscape we inhabit today.
<hr>

<p align="center">
    <img src="slides/4_top_popular_php_platforms.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ A few of Today's Most Popular Platforms

In addition to HTML and static pages, PHP, developed by Rasmus Lerdorf and released in 1995, emerged as a powerful scripting language that revolutionized web development. With its ability to generate dynamic content and interact with databases, PHP quickly became a cornerstone of web applications, powering popular platforms like WordPress, Magento, Laravel, etc.

Recognizing the significance of PHP in web hosting and content management, there is a compelling need to explore its compatibility with Android devices. By compiling PHP for the target Android platform, we can unlock a vast array of possibilities, enabling users to deploy and manage dynamic websites directly from their Android devices.

Platforms such as WordPress, Magento, and Laravel, which rely heavily on PHP, can potentially be adapted to run on Android servers, offering users unparalleled flexibility and convenience in website management. This convergence of PHP and Android opens doors to a new frontier in web hosting, allowing individuals and businesses to harness the power of these platforms on a diverse range of devices.

While the testing and results of Node.js and other JavaScript-based platforms will not be covered in this thesis for the sake of conciseness, it is worth noting their significance in the broader landscape of web development. However, the focus remains on exploring the feasibility and implications of deploying PHP-based platforms on Android devices, laying the groundwork for a deeper understanding of this evolving intersection of technology.
<hr>

<p align="center">
    <img src="slides/5_price_comparison.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ Approximate Price Comparison of Similar Architecture-based Instances in Clouds

This comparison is approximate and dated in 2019 and updated in 2021.
<hr>

<p align="center">
    <img src="slides/6_possible_use_cases.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ Possible Use Cases that Android may be of use

Considering the inherent hardware and resource constraints of Android devices, it's evident that they cannot replace the robust capabilities offered by servers powered by Intel, AMD, or Apple Silicon, especially when combined with sophisticated network infrastructure and processing power. However, recognizing the potential of Android devices for specific use cases with low resource consumption, I've curated a list of common scenarios that can be explored and benchmarked effectively.
<hr>

<p align="center">
    <img src="slides/7_android_server_diagram.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ The Initial Model is similar to Combined Clouds and Stacks in Production Servers

I've distilled the common and widely used stacks for web servers typically deployed in production environments, whether in the cloud or on virtual machines within traditional data centers. These recommendations draw from years of hands-on experience working with these technologies in various operational settings.

#### Specifications:

<ul>
    <li>Host: HUAWEI EVA-L19</li>
    <li>CPU: HiSilicon Kirin CPU, ARM, AArch64 rev 4 (aarch64) (8) @ 1.805GHz </li>
    <li>OS: Android 7.0 aarch64</li>
    <li>Kernel: 4.1.18-g29121ee</li>
    <li>Packages: 155 (dpkg), 1 (pkg)</li>
    <li>Shell: bash 5.2.2</li>
    <li>Terminal: /dev/pts/1</li>
    <li>Memory: 1680MiB / 2780MiB</li><br/>
    <li>ASN: Summit IIG, BD, APNIC</li>
    <li>Subnet: Public /32</li>
    <li>NAT: Private /24</li><br/>
    <li>Power Backup: Xiaomi 20,000 mAh</li>
</ul>
<hr>

<p align="center">
    <img src="slides/8_cost_estimation_android.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ Approximate Comparison against Target Android Server

Once again, let's compare the cost estimation against the target Android server I've been working with. One of the notable advantages is the ability to maximize server uptime using a 20,000 mAh Xiaomi Power Bank. This ARM-based device boasts exceptionally low power consumption, coupled with the advantage of low electricity costs for home use. In several consecutive tests, one full charge of the Power Bank resulted in an impressive 8 days of uninterrupted uptime.

Of course, the potential for network breaches or attacks, such as DDoS, is a concern. To mitigate these risks, I've implemented a comprehensive defense strategy. This includes utilizing Cloudflare, Mikrotik, PfSense, and Router NAT to fortify the server's perimeter. Moreover, integrating a packet-based firewall directly within the server itself would provide an additional layer of protection against such threats. Combining this with a Login Failure Daemon would further bolster security measures, although testing of this aspect is ongoing and I left for the project at this stage.
<hr>

<p align="center">
    <img src="slides/9_workflow.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ Workflow of How a Webpage Will Finally Be Served

In summary, the project involves utilizing a home network environment for hosting the target device. The server stack comprises NGINX as the web server, with SSL certificates initially issued from external sources to ensure secure communication. Additionally, PHP version 8.1 has been compiled and integrated into the stack, along with the MariaDB variant of the MySQL database. While Apache has also been compiled for potential inclusion, test results for its integration are pending to maintain focus within the scope of the work.

The culmination of these efforts involves combining all components into a cohesive server environment. Testing will encompass WordPress deployment, serving a full HTML template, and executing a single PHP script to demonstrate the PHP configurations. This comprehensive evaluation will provide valuable insights into the performance and viability of the Android-based server setup.
<hr>

<p align="center">
    <img src="slides/10_environment_samples.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ Environment Samples

Once I configured the Android device to enable external access via SSH, the majority of the work was conducted remotely using the macOS Terminal. The configuration process within the device encompassed several steps, including unlocking the bootloader, accessing recovery mode in a custom configuration, obtaining root access, and configuring Debian utilities such as Busybox. Additionally, I set up an OpenSSH server to facilitate remote access and administration of the device. These steps were crucial in establishing a robust and secure environment for managing the Android-based server remotely.
<hr>

<p align="center">
    <img src="slides/11_wordpress_processing.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ WordPress Website Processing Steps

Once a user request reaches NGINX, it acts as the web server and communicates with the PHP socket running in the background. This PHP socket enables the execution of WordPress PHP scripts, which in turn interact with the MySQL database server in the background. This communication pathway ensures seamless handling of user requests, dynamic content generation, and database interactions within the WordPress environment hosted on the Android server.
<hr>

<p align="center">
    <img src="slides/12_end_result_pages.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ WordPress Pages

To provide visual evidence of the successful implementation of the WordPress website on the Android server, screenshots of key pages are essential. These include:

1. WordPress Homepage: This screenshot showcases the main landing page of the WordPress website, demonstrating its accessibility and proper rendering on various devices.

2. User Registration Page: A screenshot of the user registration page validates the functionality of user account creation, a fundamental feature of WordPress websites.

3. Profile Page: Displaying a screenshot of the user profile page confirms that users can access and modify their profile information, contributing to a personalized user experience.

Additionally, incorporating a forum plugin into WordPress and capturing screenshots of forum-related pages further demonstrates the versatility and functionality of the WordPress installation on the Android server.

These screenshots serve as tangible evidence of the successful deployment and functionality of the WordPress website on the Android server, reinforcing the findings and conclusions of the thesis project.
<hr>

<p align="center">
    <img src="slides/13_more_pages.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ HTML Template page and PHPINFO single PHP Page

Additional screenshots of specific target tests regarding static HTML pages and a single PHP Script enhance the comprehensiveness of the project documentation. Here are two additional target tests for which screenshots are provided as to how they look.

<hr>

<p align="center">
    <img src="slides/14_benchmark_wordpress.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ Requests vs Time result

Comparison of Requests vs. Response Times Benchmark Results

The benchmark tests presented herein were conducted using the Apache benchmark tool from various devices outside the home network.

<p align="center">
    <img src="slides/15_benchmark_html.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>


<p align="center">
    <img src="slides/16_benchmark_php.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>


<p align="center">
    <img src="slides/17_request_processing_comparison.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ A Comparison of performances and responses together

I aggregated the results to provide a comprehensive overview of how Android performed in terms of requests over time, with the constraint that requests were limited to 1000.
<hr>

<p align="center">
    <img src="slides/18_further_cases.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ Further Case Possibilities

The tests were not executed, but it's worth exploring the potential scenarios where Android can complement high-end servers, balancing loads to enhance performance and isolating instances in cloud environments.
<hr>

<p align="center">
    <img src="slides/19_references.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ References

Acknowledgments to the Major Utilities Utilized Throughout the Testing for This Thesis Project:

I would like to extend my sincere gratitude to the major utilities that played a pivotal role in conducting the testing for this thesis project. Special thanks to the Apache benchmark tool for facilitating accurate performance measurements and analysis. Additionally, I express my appreciation to the WordPress CMS for providing a robust platform for website deployment and management. Without the contributions of these utilities, this research endeavor would not have been possible.
<hr>

<p align="center">
    <img src="slides/20_end.png" alt="Ibrahim Sharif Android Server WordPress" />
</p>

### ❖ Futher Discussion

For further improvements, ongoing work, and any questions a Discussion Section has been established to facilitate collaboration and exchange of ideas. Thank you for your interest and participation.
[10-02-2024]
<hr>