
%question 1st

matrix1 = randi([1, 10], 3, 4);
matrix2 = randi([1, 10], 3, 4);

% 1) multiplication
elementwise_product = matrix1 .* matrix2;

% 2) summation
elementwise_sum = matrix1 + matrix2;

% 3)  division
elementwise_ratio = matrix1 ./ matrix2;

% 4) Remove 1st and 2nd column of the output obtained in (3)
modified_ratio_output = elementwise_ratio(:, 3:end);

% 5) Replace the 1st row in (i) with an array: 1, 2, 3, 4
elementwise_product(1, :) = [1, 2, 3, 4];


% (vi) Divide the output in (iii) by the number 7
division_by_7 = elementwise_ratio / 7;



disp('(i) Element-wise multiplication: ');
disp(elementwise_product);

disp('(ii) Element-wise summation: ');
disp(elementwise_sum);

disp('(iii) Element-wise division: ');
disp(elementwise_ratio);

disp('(iv) Modified output after removing 1st and 2nd column: ');
disp(modified_ratio_output);

disp('(v) Matrix after replacing the 1st row in (i): ');
disp(elementwise_product);

disp('(vi) Division of output in (iii) by 7: ');
disp(division_by_7);




%question 2 
% Create vector v with elements 1 through 10
v = 1:10;

% i) x = v
x = v  .* v;

% ii) y = v/(v-1)
%v=1 is not valid 
y = v./(v - 1);

% iii) z = 3v
z = 3 * v;

% iv) w = 3(1-v)
w = 3 * (1 - v);

% v) u = 3v + 1 + v
u = 3 * v + 1 + v;

% results
disp('1) x = ');
disp(x);

disp('2) y = ');
disp(y);

disp('3) z = ');
disp(z);

disp('4) w = ');
disp(w);

disp('5) u = ');
disp(u);





%qusetion 3
% Create vector v with elements 1 through 10
v = 1:10;

% i) x = v
x = v .* v;


% v=1 is not included
y = v./(v - 1);

figure;


subplot(2, 1, 1);
plot(v, x, '-o');
title('Plot of x with respect to v');
xlabel('v');
ylabel('x');

subplot(2, 1, 2);
plot(v, y, '-o');
title('Plot of y with respect to v');
xlabel('v');
ylabel('y');


sgtitle('Plots of x and y withrespect to v');



%question 4

% Define vectors x and y
x = [0, 5, 7];
y = [0, 2, 8];

% i)
m = (x > y) & (x > 4);

% ii)
n = x | y;

% iii)
o = ~(x | y);

% iv) 
p = x .* y;

% v) 
q = x ./ y;

% vi)
r = x.^y;


disp('i) m = ');
disp(m);

disp('ii) n = ');
disp(n);

disp('iii) o = ');
disp(o);

disp('iv) p = ');
disp(p);

disp('v) q = ');
disp(q);

disp('vi) r = ');
disp(r);





%question 5 

v = -0.2:0.02:2;


disp('Vector v:');
disp(v);





%question 6


imagePath = 'C:\Users\vedant kasar\Downloads\pomsky-puppy-791798.jpg'; 

% Load the image
img = imread(imagePath);

% Display the image
figure;
imshow(img);
title('Captured Image');




%question 7

audioFilePath = 'C:\Users\vedant kasar\Downloads'; 

[y, Fs] = audioread(audioFilePath);

% waveform
figure;
plot((1:length(y))/Fs, y);
xlabel('Time (seconds)');
ylabel('Amplitude');
title('Waveform of the Audio');

% audio
sound(y, Fs);















